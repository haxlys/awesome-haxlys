# awesome-haxlys 에이전트 설정

## 프로젝트 설명

haxlys 계정의 GitHub starred 레포 중 AI 개발과 에이전트 워크플로 관점에서 선별한 큐레이션 리스트.

## 스킬

- [update-starred-repos](.agents/skills/update-starred-repos/SKILL.md) — GitHub API로 스타 레포를 조회해 README를 최신화 (범용)
- [update-starred-repos (OpenCode)](.opencode/skills/update-starred-repos/SKILL.md) — OpenCode 전용 variant

## 작업 규칙

- README 엔트리는 한국어 설명
- star 수는 GraphQL 또는 REST API 실측값 기준
- README 상단에 `마지막 업데이트: YYYY-MM-DD` 유지
