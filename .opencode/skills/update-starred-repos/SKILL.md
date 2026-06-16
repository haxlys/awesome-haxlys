# awesome-haxlys 스타 레포 업데이트 스킬

haxlys 계정의 GitHub starred 레포를 조회해 `README.md`에 반영합니다.

## 트리거

- "별표한 레포 최신화"
- "README 업데이트"
- "스타 레포 추가"
- "update starred repos"
- "sync stars"

## 워크플로

### 1. GitHub API로 스타 레포 전체 조회

```bash
# GraphQL — 최신 100개 (starredAt 내림차순)
gh api graphql -f query='
query {
  viewer {
    starredRepositories(first: 100, orderBy: {field: STARRED_AT, direction: DESC}) {
      pageInfo { hasNextPage endCursor }
      totalCount
      edges {
        starredAt
        node {
          nameWithOwner
          stargazerCount
          primaryLanguage { name }
          description
        }
      }
    }
  }
}' --jq '
  "총 \(.data.viewer.starredRepositories.totalCount)개",
  (.data.viewer.starredRepositories.edges[] |
    "\(.starredAt[0:10]) | \(.node.stargazerCount)⭐ | \(.node.primaryLanguage.name // "-") | \(.node.nameWithOwner) | \(.node.description // "")")
'
```

> ⚠️ `starredAt`은 REST API 대신 **GraphQL**로만 조회 가능. REST의 `GET /user/starred`는 `starred_at`이 null로 반환됨.

### 2. README에 없는 신규 레포 식별

README의 마지막 업데이트 날짜를 확인하고(`마지막 업데이트: YYYY-MM-DD`), 그 이후 `starredAt`인 레포 중 README에 없는 것만 선별.

README에 이미 있는 레포인지 확인:

```bash
grep "owner/repo" README.md
```

### 3. 신규 레포 분류

README의 16개 카테고리(하위 카테고리 포함) 중 적합한 곳에 배치. 분류 기준:

| 카테고리 | 포함 대상 |
|---|---|
| 자율 AI 에이전트와 실행 환경 | Hermes, OpenClaw 같은 자율 에이전트 |
| AI 코딩 에이전트와 실행 환경 | 코딩 전용 에이전트/하네스 |
| AI 코딩 에이전트 운영과 PR 자동화 | 오케스트레이션, PR, 코드 리뷰 |
| 스펙 기반 개발과 계획 도구 | OpenSpec, spec-kit 등 |
| 에이전트 스킬, 프롬프트, 운영 가이드 | 스킬 모음, 프롬프트, 설정 |
| 멀티 에이전트 프레임워크와 플랫폼 | Autogen, CrewAI 등 |
| 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 메모리, 검색, 지식 그래프 |
| LLM 서빙, 로컬 모델, 게이트웨이 | vLLM, ollama, LiteLLM 등 |
| AI 앱, 채팅 UI, 워크플로 빌더 | Dify, n8n, LobeHub 등 |
| MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | MCP 서버, 브라우저 도구, CLI 도구 |
| 개발 생산성/CLI 도구 | Lazygit 등 개발 효율 도구 |
| 디자인, UI 생성, 프로토타이핑 | Penpot, open-design 등 |
| 프론트엔드, 웹 프레임워크, 앱 라이브러리 | React 라이브러리, 차트, CSS |
| 보안, 평가, 관측성, 품질 | Langfuse, PromptFoo 등 |
| 학습, 연구, Awesome 목록, 참고자료 | 튜토리얼, awesome-list |
| 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 영상, 음성, 데스크톱 앱 |
| 법률, 금융, 크립토, 기타 | 트레이딩, 법률, 암호화폐 |

### 4. 기존 레포 star 수 최신화

```bash
# README에서 전체 레포 이름 추출 (196개)
grep -o 'github\.com/[^)]*' README.md | sed 's|github\.com/||' | sort -u > /tmp/repo_names.txt

# 각 레포의 현재 star 수 조회 (병렬)
awk -F/ '{print "https://api.github.com/repos/"$1"/"$2}' /tmp/repo_names.txt \
  | xargs -P 8 -I{} sh -c 'curl -s -H "Authorization: token $(gh auth token)" "{}" | jq -r "[.full_name, (.stargazers_count|tostring)] | join(\"|\")"' \
  > /tmp/star_counts.txt
```

그 후 README에서 정규식 `(⭐ [0-9,]+)`를 새 값으로 치환.

### 5. README 편집 규칙

**엔트리 형식** (기존 형식 엄격 유지):
```markdown
- YYYY-MM-DD - [owner/repo](https://github.com/owner/repo) (⭐ 123,456) - Language - 한국어 설명
```

- 언어가 `Unknown`이거나 없는 경우: `- 한국어 설명` (언어 생략)
- 날짜는 `starredAt`의 `YYYY-MM-DD`
- star 수는 `stargazers_count`를 천 단위 콤마로 포맷
- 설명은 한국어, 레포 description을 참고해 1줄로 작성

**변경해야 할 항목**:
1. 헤더: `마지막 업데이트: YYYY-MM-DD`, 총 스타 수
2. 빠른 탐색: 카테고리별 카운트와 앵커 링크
3. 각 섹션 헤더: 카테고리명 (새 카운트)
4. 기존 엔트리: star 수 최신화
5. 신규 엔트리: 날짜 내림차순 삽입 (각 섹션 또는 하위 섹션 첫 줄에 최신 날짜)

### 6. 검증

```bash
# 엔트리 총 개수 확인
grep -c 'github\.com/' README.md

# 중복 체크
grep -o 'github\.com/[^)]*' README.md | sort | uniq -d

# 앵커와 섹션 카운트 일치 확인
grep '^### ' README.md
grep '^- \[' README.md | head -20
```

## 메모

- 이 스킬은 GraphQL API를 사용하므로 `gh` 인증 필요 (`gh auth status`)
- `starred_at`이 null인 항목은 GraphQL 쿼리에서 `starredAt`이 없음을 의미하므로 필터
- star 수는 실시간 스냅샷이므로 세션마다 다를 수 있음
- 카테고리 분류가 어려운 레포는 기존 README의 유사 레포 참고
