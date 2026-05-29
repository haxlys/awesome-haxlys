# awesome-haxlys 카테고리 전수 감사

- 감사일: 2026-05-29
- 기준 파일: README.md (감사 당시 카테고리 기준)
- 대상: README에 수록된 GitHub 레포 172개
- 최신 메타데이터 수집: GitHub GraphQL/API (2026-05-29T06:41:02.831Z)
- 보강 확인: 주요 재분류 후보는 GitHub README, 공식 문서/사이트, 웹 검색 결과로 재확인
- 반영 상태: 강한 이동 권고 6개는 2026-05-29 README.md에 반영됨

## 결론

- 강한 이동 권고: 6개
- 이동 검토 후보: 12개
- 현 위치 유지 권고: 154개
- GitHub API 기준 접근 실패 레포: 0개
- GitHub API 기준 fork 표시 레포: 1개 (`Glass-HQ/Glass`, Zed fork임을 README에서 명시)

## 판단 기준

- 레포가 제공하는 “주된 사용자 가치”를 기술 스택보다 우선했다.
- 도메인 특화 레포는 일반 에이전트 구조보다 도메인 카테고리를 우선했다. 예: 금융 에이전트는 멀티 에이전트보다 금융 카테고리.
- 설치 가능한 skill, prompt, persona, guide 모음은 `에이전트 스킬, 프롬프트, 운영 가이드`로 보았다.
- 실제 실행 프레임워크나 런타임은 `자율 AI 에이전트`, `AI 코딩 에이전트`, `멀티 에이전트` 계열로 보았다.
- 측정, 평가, 보안, 관측, 품질 관리가 핵심이면 `보안, 평가, 관측성, 품질`로 보았다.
- 영상/음성/문서 변환/네이티브 앱/모바일/데스크톱 유틸리티는 `네이티브, 미디어, 모바일/데스크톱 유틸리티`로 보았다.
- awesome 목록, 튜토리얼, 연구 벤치마크, 교육 자료는 `학습, 연구, Awesome 목록, 참고자료`로 보았다.

## 강한 이동 권고

| 레포 | 감사 당시 카테고리 | 권장 카테고리 | 이유 |
|---|---|---|---|
| [anthropics/claude-code-action](https://github.com/anthropics/claude-code-action) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | AI 코딩 에이전트 운영과 PR 자동화 | GitHub PR/이슈에서 Claude Code를 실행해 리뷰, 구현, 자동화 작업을 수행하는 GitHub Action이다. |
| [davebcn87/pi-autoresearch](https://github.com/davebcn87/pi-autoresearch) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | AI 코딩 에이전트 운영과 PR 자동화 | pi 코딩 에이전트 확장으로 실험 실행, 커밋, keep/revert를 반복하는 자율 최적화 루프가 핵심이다. |
| [understudy-ai/understudy](https://github.com/understudy-ai/understudy) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 자율 AI 에이전트와 실행 환경 | GUI, 브라우저, 셸, 메시징 앱을 한 지시로 조작하는 로컬 자율 컴퓨터 사용 에이전트다. |
| [nibzard/awesome-agentic-patterns](https://github.com/nibzard/awesome-agentic-patterns) | 멀티 에이전트 프레임워크와 플랫폼 | 학습, 연구, Awesome 목록, 참고자료 | 실행 프레임워크가 아니라 에이전트 패턴을 모은 curated catalogue와 참고 사이트다. |
| [msitarzewski/agency-agents](https://github.com/msitarzewski/agency-agents) | 멀티 에이전트 프레임워크와 플랫폼 | 에이전트 스킬, 프롬프트, 운영 가이드 | 런타임 프레임워크라기보다 Claude Code, Copilot, OpenClaw 등에 설치하는 Markdown 에이전트 페르소나 모음이다. |
| [cloudflare/telescope](https://github.com/cloudflare/telescope) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 보안, 평가, 관측성, 품질 | 브라우저별 Web Vitals, HAR, 콘솔, 리소스 타이밍, 스크린샷/필름스트립을 수집하는 성능 테스트/관측 도구다. |

## 이동 검토 후보

아래는 “틀렸다”보다는 “다른 기준을 택하면 더 자연스러울 수 있는” 항목이다. 현재 카테고리 유지도 가능한 항목을 포함했다.

| 레포 | 감사 당시 카테고리 | 검토 후보 | 판단 |
|---|---|---|---|
| [TanStack/cli](https://github.com/TanStack/cli) | 에이전트 스킬, 프롬프트, 운영 가이드 | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 최신 README는 TanStack Router/Start 앱 생성과 add-on 관리가 중심이다. 다만 MCP/AI toolkit 성격도 있어 현 위치도 완전히 틀리진 않다. |
| [ultroned/xray-react](https://github.com/ultroned/xray-react) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | AI/MCP 도구라기보다 React 컴포넌트 구조를 보여주고 에디터로 이동시키는 React 개발 디버깅 도구다. |
| [aidenybai/react-grab](https://github.com/aidenybai/react-grab) | 디자인, UI 생성, 프로토타이핑 | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | UI 요소를 복사해 에이전트에 소스 컨텍스트로 전달하는 개발/에이전트 보조 도구다. UI 제작 흐름이라 현재 디자인 카테고리도 허용 가능하다. |
| [Cocoon-AI/architecture-diagram-generator](https://github.com/Cocoon-AI/architecture-diagram-generator) | 디자인, UI 생성, 프로토타이핑 | 에이전트 스킬, 프롬프트, 운영 가이드 | Claude AI skill이지만 산출물이 아키텍처 다이어그램이라 디자인 카테고리 유지도 가능하다. |
| [jakubkrehel/make-interfaces-feel-better](https://github.com/jakubkrehel/make-interfaces-feel-better) | 에이전트 스킬, 프롬프트, 운영 가이드 | 디자인, UI 생성, 프로토타이핑 | 내용은 UI 디자인 디테일이지만 배포 단위는 Agent Skill이다. 현재 전문 도메인 스킬 위치가 더 일관적일 수 있다. |
| [mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill) | 에이전트 스킬, 프롬프트, 운영 가이드 | 학습, 연구, Awesome 목록, 참고자료 | 최근 30일 리서치를 수행하지만 repo 형태는 AI agent skill이다. 현재 스킬 카테고리 유지가 자연스럽다. |
| [robertpiosik/CodeWebChat](https://github.com/robertpiosik/CodeWebChat) | AI 앱, 채팅 UI, 워크플로 빌더 | AI 코딩 에이전트와 실행 환경 | VS Code용 AI 코딩 툴킷이다. 다만 사용자-facing AI 앱/코딩 앱으로 보는 현 위치도 가능하다. |
| [microsoft/apm](https://github.com/microsoft/apm) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 에이전트 스킬, 프롬프트, 운영 가이드 | 스킬/프롬프트/플러그인 의존성을 관리하지만 CLI/패키지 매니저이므로 현 에이전트 도구 카테고리도 적합하다. |
| [chrisryugj/kordoc](https://github.com/chrisryugj/kordoc) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 문서 파서 CLI + MCP 서버라 에이전트 도구로도 볼 수 있다. HWP/PDF/Office 변환 유틸리티라 현 미디어/유틸 위치도 적합하다. |
| [facebookresearch/ProgramBench](https://github.com/facebookresearch/ProgramBench) | 학습, 연구, Awesome 목록, 참고자료 | 보안, 평가, 관측성, 품질 | 언어 모델 평가 벤치마크지만 연구 성격이 강해 현재 학습/연구 카테고리도 맞다. |
| [TauricResearch/TradingAgents](https://github.com/TauricResearch/TradingAgents) | 법률, 금융, 크립토, 기타 | 멀티 에이전트 프레임워크와 플랫폼 | 멀티 에이전트 프레임워크이지만 금융 트레이딩 도메인이 핵심이라 현재 법률/금융/크립토 도메인 카테고리 유지가 낫다. |
| [virattt/ai-hedge-fund](https://github.com/virattt/ai-hedge-fund) | 법률, 금융, 크립토, 기타 | 멀티 에이전트 프레임워크와 플랫폼 | AI 에이전트 팀 구조지만 헤지펀드/투자 의사결정 도메인이 핵심이라 현재 금융 카테고리 유지가 낫다. |

## 전체 레포 판정표

| # | 레포 | 감사 당시 카테고리 | 판정 | 권장/비고 |
|---:|---|---|---|---|
| 1 | [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) | 자율 AI 에이전트와 실행 환경 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 2 | [openclaw/openclaw](https://github.com/openclaw/openclaw) | 자율 AI 에이전트와 실행 환경 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 3 | [ultraworkers/claw-code](https://github.com/ultraworkers/claw-code) | AI 코딩 에이전트와 실행 환경 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 4 | [langchain-ai/open-swe](https://github.com/langchain-ai/open-swe) | AI 코딩 에이전트와 실행 환경 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 5 | [earendil-works/pi](https://github.com/earendil-works/pi) | AI 코딩 에이전트와 실행 환경 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 6 | [code-yeongyu/oh-my-openagent](https://github.com/code-yeongyu/oh-my-openagent) | AI 코딩 에이전트와 실행 환경 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 7 | [anomalyco/opencode](https://github.com/anomalyco/opencode) | AI 코딩 에이전트와 실행 환경 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 8 | [ruvnet/ruflo](https://github.com/ruvnet/ruflo) | AI 코딩 에이전트 운영과 PR 자동화 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 9 | [multica-ai/multica](https://github.com/multica-ai/multica) | AI 코딩 에이전트 운영과 PR 자동화 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 10 | [paperclipai/paperclip](https://github.com/paperclipai/paperclip) | AI 코딩 에이전트 운영과 PR 자동화 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 11 | [jonwiggins/optio](https://github.com/jonwiggins/optio) | AI 코딩 에이전트 운영과 PR 자동화 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 12 | [ComposioHQ/agent-orchestrator](https://github.com/ComposioHQ/agent-orchestrator) | AI 코딩 에이전트 운영과 PR 자동화 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 13 | [openai/symphony](https://github.com/openai/symphony) | AI 코딩 에이전트 운영과 PR 자동화 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 14 | [klawsh/klaw.sh](https://github.com/klawsh/klaw.sh) | AI 코딩 에이전트 운영과 PR 자동화 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 15 | [gastownhall/gastown](https://github.com/gastownhall/gastown) | AI 코딩 에이전트 운영과 PR 자동화 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 16 | [Fission-AI/OpenSpec](https://github.com/Fission-AI/OpenSpec) | 스펙 기반 개발과 계획 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 17 | [gszhangwei/open-spdd](https://github.com/gszhangwei/open-spdd) | 스펙 기반 개발과 계획 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 18 | [github/spec-kit](https://github.com/github/spec-kit) | 스펙 기반 개발과 계획 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 19 | [mattpocock/skills](https://github.com/mattpocock/skills) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 20 | [cloudflare/skills](https://github.com/cloudflare/skills) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 21 | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 22 | [anthropics/skills](https://github.com/anthropics/skills) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 23 | [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 24 | [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 25 | [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 26 | [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 27 | [elder-plinius/CL4R1T4S](https://github.com/elder-plinius/CL4R1T4S) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 28 | [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 29 | [shanraisshan/claude-code-best-practice](https://github.com/shanraisshan/claude-code-best-practice) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 30 | [alinaqi/claude-bootstrap](https://github.com/alinaqi/claude-bootstrap) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 31 | [luongnv89/claude-howto](https://github.com/luongnv89/claude-howto) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 32 | [diet103/claude-code-infrastructure-showcase](https://github.com/diet103/claude-code-infrastructure-showcase) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 33 | [PatrickJS/awesome-cursorrules](https://github.com/PatrickJS/awesome-cursorrules) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 34 | [jakubkrehel/make-interfaces-feel-better](https://github.com/jakubkrehel/make-interfaces-feel-better) | 에이전트 스킬, 프롬프트, 운영 가이드 | 검토 | 디자인, UI 생성, 프로토타이핑도 가능 - 내용은 UI 디자인 디테일이지만 배포 단위는 Agent Skill이다. 현재 전문 도메인 스킬 위치가 더 일관적일 수 있다. |
| 35 | [SimoneAvogadro/android-reverse-engineering-skill](https://github.com/SimoneAvogadro/android-reverse-engineering-skill) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 36 | [ericosiu/ai-marketing-skills](https://github.com/ericosiu/ai-marketing-skills) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 37 | [phuryn/pm-skills](https://github.com/phuryn/pm-skills) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 38 | [mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill) | 에이전트 스킬, 프롬프트, 운영 가이드 | 검토 | 학습, 연구, Awesome 목록, 참고자료도 가능 - 최근 30일 리서치를 수행하지만 repo 형태는 AI agent skill이다. 현재 스킬 카테고리 유지가 자연스럽다. |
| 39 | [garrytan/gbrain](https://github.com/garrytan/gbrain) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 40 | [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 41 | [garrytan/gstack](https://github.com/garrytan/gstack) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 42 | [obra/superpowers](https://github.com/obra/superpowers) | 에이전트 스킬, 프롬프트, 운영 가이드 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 43 | [TanStack/cli](https://github.com/TanStack/cli) | 에이전트 스킬, 프롬프트, 운영 가이드 | 검토 | 프론트엔드, 웹 프레임워크, 앱 라이브러리도 가능 - 최신 README는 TanStack Router/Start 앱 생성과 add-on 관리가 중심이다. 다만 MCP/AI toolkit 성격도 있어 현 위치도 완전히 틀리진 않다. |
| 44 | [microsoft/autogen](https://github.com/microsoft/autogen) | 멀티 에이전트 프레임워크와 플랫폼 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 45 | [agentscope-ai/agentscope](https://github.com/agentscope-ai/agentscope) | 멀티 에이전트 프레임워크와 플랫폼 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 46 | [mikeyobrien/ralph-orchestrator](https://github.com/mikeyobrien/ralph-orchestrator) | 멀티 에이전트 프레임워크와 플랫폼 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 47 | [crewAIInc/crewAI](https://github.com/crewAIInc/crewAI) | 멀티 에이전트 프레임워크와 플랫폼 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 48 | [bytedance/deer-flow](https://github.com/bytedance/deer-flow) | 멀티 에이전트 프레임워크와 플랫폼 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 49 | [msitarzewski/agency-agents](https://github.com/msitarzewski/agency-agents) | 멀티 에이전트 프레임워크와 플랫폼 | 이동 권고 | 에이전트 스킬, 프롬프트, 운영 가이드 - 런타임 프레임워크라기보다 Claude Code, Copilot, OpenClaw 등에 설치하는 Markdown 에이전트 페르소나 모음이다. |
| 50 | [langchain-ai/langchain](https://github.com/langchain-ai/langchain) | 멀티 에이전트 프레임워크와 플랫폼 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 51 | [nibzard/awesome-agentic-patterns](https://github.com/nibzard/awesome-agentic-patterns) | 멀티 에이전트 프레임워크와 플랫폼 | 이동 권고 | 학습, 연구, Awesome 목록, 참고자료 - 실행 프레임워크가 아니라 에이전트 패턴을 모은 curated catalogue와 참고 사이트다. |
| 52 | [nex-crm/wuphf](https://github.com/nex-crm/wuphf) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 53 | [alash3al/stash](https://github.com/alash3al/stash) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 54 | [letta-ai/letta-code](https://github.com/letta-ai/letta-code) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 55 | [MemPalace/mempalace](https://github.com/MemPalace/mempalace) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 56 | [topoteretes/cognee](https://github.com/topoteretes/cognee) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 57 | [thedotmack/claude-mem](https://github.com/thedotmack/claude-mem) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 58 | [proxysoul/soulforge](https://github.com/proxysoul/soulforge) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 59 | [VectifyAI/PageIndex](https://github.com/VectifyAI/PageIndex) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 60 | [abhigyanpatwari/GitNexus](https://github.com/abhigyanpatwari/GitNexus) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 61 | [zilliztech/claude-context](https://github.com/zilliztech/claude-context) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 62 | [tirth8205/code-review-graph](https://github.com/tirth8205/code-review-graph) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 63 | [marcoaapfortes/Mantic.sh](https://github.com/marcoaapfortes/Mantic.sh) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 64 | [upstash/context7](https://github.com/upstash/context7) | 에이전트 메모리, 컨텍스트, RAG, 코드 인텔리전스 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 65 | [raullenchai/Rapid-MLX](https://github.com/raullenchai/Rapid-MLX) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 66 | [vllm-project/vllm](https://github.com/vllm-project/vllm) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 67 | [antirez/ds4](https://github.com/antirez/ds4) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 68 | [ollama/ollama](https://github.com/ollama/ollama) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 69 | [nicedreamzapp/claude-code-local](https://github.com/nicedreamzapp/claude-code-local) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 70 | [kessler/gemma-gem](https://github.com/kessler/gemma-gem) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 71 | [AlexsJones/llmfit](https://github.com/AlexsJones/llmfit) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 72 | [microsoft/BitNet](https://github.com/microsoft/BitNet) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 73 | [sauravpanda/BrowserAI](https://github.com/sauravpanda/BrowserAI) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 74 | [ENTERPILOT/GoModel](https://github.com/ENTERPILOT/GoModel) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 75 | [tensorzero/tensorzero](https://github.com/tensorzero/tensorzero) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 76 | [BerriAI/litellm](https://github.com/BerriAI/litellm) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 77 | [diegosouzapw/OmniRoute](https://github.com/diegosouzapw/OmniRoute) | LLM 서빙, 로컬 모델, 게이트웨이 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 78 | [lobehub/lobehub](https://github.com/lobehub/lobehub) | AI 앱, 채팅 UI, 워크플로 빌더 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 79 | [langgenius/dify](https://github.com/langgenius/dify) | AI 앱, 채팅 UI, 워크플로 빌더 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 80 | [langflow-ai/langflow](https://github.com/langflow-ai/langflow) | AI 앱, 채팅 UI, 워크플로 빌더 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 81 | [open-webui/open-webui](https://github.com/open-webui/open-webui) | AI 앱, 채팅 UI, 워크플로 빌더 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 82 | [n8n-io/n8n](https://github.com/n8n-io/n8n) | AI 앱, 채팅 UI, 워크플로 빌더 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 83 | [pingdotgg/t3code](https://github.com/pingdotgg/t3code) | AI 앱, 채팅 UI, 워크플로 빌더 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 84 | [companion-inc/feynman](https://github.com/companion-inc/feynman) | AI 앱, 채팅 UI, 워크플로 빌더 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 85 | [karpathy/nanochat](https://github.com/karpathy/nanochat) | AI 앱, 채팅 UI, 워크플로 빌더 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 86 | [cloudflare/vibesdk](https://github.com/cloudflare/vibesdk) | AI 앱, 채팅 UI, 워크플로 빌더 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 87 | [robertpiosik/CodeWebChat](https://github.com/robertpiosik/CodeWebChat) | AI 앱, 채팅 UI, 워크플로 빌더 | 검토 | AI 코딩 에이전트와 실행 환경도 가능 - VS Code용 AI 코딩 툴킷이다. 다만 사용자-facing AI 앱/코딩 앱으로 보는 현 위치도 가능하다. |
| 88 | [assistant-ui/assistant-ui](https://github.com/assistant-ui/assistant-ui) | AI 앱, 채팅 UI, 워크플로 빌더 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 89 | [ibelick/prompt-kit](https://github.com/ibelick/prompt-kit) | AI 앱, 채팅 UI, 워크플로 빌더 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 90 | [getsentry/XcodeBuildMCP](https://github.com/getsentry/XcodeBuildMCP) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 91 | [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 92 | [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 93 | [modelcontextprotocol/typescript-sdk](https://github.com/modelcontextprotocol/typescript-sdk) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 94 | [AgentDeskAI/browser-tools-mcp](https://github.com/AgentDeskAI/browser-tools-mcp) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 95 | [vercel-labs/agent-browser](https://github.com/vercel-labs/agent-browser) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 96 | [lightpanda-io/browser](https://github.com/lightpanda-io/browser) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 97 | [D4Vinci/Scrapling](https://github.com/D4Vinci/Scrapling) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 98 | [web-infra-dev/midscene](https://github.com/web-infra-dev/midscene) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 99 | [browserbase/stagehand](https://github.com/browserbase/stagehand) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 100 | [magnitudedev/browser-agent](https://github.com/magnitudedev/browser-agent) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 101 | [lahfir/agent-desktop](https://github.com/lahfir/agent-desktop) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 102 | [junhoyeo/tokscale](https://github.com/junhoyeo/tokscale) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 103 | [dmtrKovalenko/fff](https://github.com/dmtrKovalenko/fff) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 104 | [jackwener/OpenCLI](https://github.com/jackwener/OpenCLI) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 105 | [microsoft/apm](https://github.com/microsoft/apm) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 검토 | 에이전트 스킬, 프롬프트, 운영 가이드도 가능 - 스킬/프롬프트/플러그인 의존성을 관리하지만 CLI/패키지 매니저이므로 현 에이전트 도구 카테고리도 적합하다. |
| 106 | [HKUDS/CLI-Anything](https://github.com/HKUDS/CLI-Anything) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 107 | [x-cmd/x-cmd](https://github.com/x-cmd/x-cmd) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 108 | [googleworkspace/cli](https://github.com/googleworkspace/cli) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 109 | [mmarinovic/React2AWS](https://github.com/mmarinovic/React2AWS) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 110 | [punkpeye/pipenet](https://github.com/punkpeye/pipenet) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 111 | [ultroned/xray-react](https://github.com/ultroned/xray-react) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 검토 | 프론트엔드, 웹 프레임워크, 앱 라이브러리도 가능 - AI/MCP 도구라기보다 React 컴포넌트 구조를 보여주고 에디터로 이동시키는 React 개발 디버깅 도구다. |
| 112 | [huseyinbabal/taws](https://github.com/huseyinbabal/taws) | MCP, 브라우저/데스크톱 자동화, 에이전트 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 113 | [jesseduffield/lazygit](https://github.com/jesseduffield/lazygit) | 개발 생산성/CLI 도구 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 114 | [nexu-io/open-design](https://github.com/nexu-io/open-design) | 디자인, UI 생성, 프로토타이핑 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 115 | [penpot/penpot](https://github.com/penpot/penpot) | 디자인, UI 생성, 프로토타이핑 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 116 | [Cocoon-AI/architecture-diagram-generator](https://github.com/Cocoon-AI/architecture-diagram-generator) | 디자인, UI 생성, 프로토타이핑 | 검토 | 에이전트 스킬, 프롬프트, 운영 가이드도 가능 - Claude AI skill이지만 산출물이 아키텍처 다이어그램이라 디자인 카테고리 유지도 가능하다. |
| 117 | [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) | 디자인, UI 생성, 프로토타이핑 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 118 | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | 디자인, UI 생성, 프로토타이핑 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 119 | [open-pencil/open-pencil](https://github.com/open-pencil/open-pencil) | 디자인, UI 생성, 프로토타이핑 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 120 | [vibeflowing-inc/vibe_figma](https://github.com/vibeflowing-inc/vibe_figma) | 디자인, UI 생성, 프로토타이핑 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 121 | [pqoqubbw/icons](https://github.com/pqoqubbw/icons) | 디자인, UI 생성, 프로토타이핑 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 122 | [aidenybai/react-grab](https://github.com/aidenybai/react-grab) | 디자인, UI 생성, 프로토타이핑 | 검토 | MCP, 브라우저/데스크톱 자동화, 에이전트 도구도 가능 - UI 요소를 복사해 에이전트에 소스 컨텍스트로 전달하는 개발/에이전트 보조 도구다. UI 제작 흐름이라 현재 디자인 카테고리도 허용 가능하다. |
| 123 | [open-circle/valibot](https://github.com/open-circle/valibot) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 124 | [davebcn87/pi-autoresearch](https://github.com/davebcn87/pi-autoresearch) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 이동 권고 | AI 코딩 에이전트 운영과 PR 자동화 - pi 코딩 에이전트 확장으로 실험 실행, 커밋, keep/revert를 반복하는 자율 최적화 루프가 핵심이다. |
| 125 | [understudy-ai/understudy](https://github.com/understudy-ai/understudy) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 이동 권고 | 자율 AI 에이전트와 실행 환경 - GUI, 브라우저, 셸, 메시징 앱을 한 지시로 조작하는 로컬 자율 컴퓨터 사용 에이전트다. |
| 126 | [DavidHDev/react-bits](https://github.com/DavidHDev/react-bits) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 127 | [aidenybai/react-scan](https://github.com/aidenybai/react-scan) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 128 | [cloudflare/telescope](https://github.com/cloudflare/telescope) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 이동 권고 | 보안, 평가, 관측성, 품질 - 브라우저별 Web Vitals, HAR, 콘솔, 리소스 타이밍, 스크린샷/필름스트립을 수집하는 성능 테스트/관측 도구다. |
| 129 | [palantir/blueprint](https://github.com/palantir/blueprint) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 130 | [3ru/eslint-plugin-baseline-js](https://github.com/3ru/eslint-plugin-baseline-js) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 131 | [anthropics/claude-code-action](https://github.com/anthropics/claude-code-action) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 이동 권고 | AI 코딩 에이전트 운영과 PR 자동화 - GitHub PR/이슈에서 Claude Code를 실행해 리뷰, 구현, 자동화 작업을 수행하는 GitHub Action이다. |
| 132 | [privatenumber/minification-benchmarks](https://github.com/privatenumber/minification-benchmarks) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 133 | [AlexSergey/rockpack](https://github.com/AlexSergey/rockpack) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 134 | [fastify/fastify-vite](https://github.com/fastify/fastify-vite) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 135 | [e18e/e18e](https://github.com/e18e/e18e) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 136 | [bigskysoftware/htmx](https://github.com/bigskysoftware/htmx) | 프론트엔드, 웹 프레임워크, 앱 라이브러리 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 137 | [vercel-labs/deepsec](https://github.com/vercel-labs/deepsec) | 보안, 평가, 관측성, 품질 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 138 | [langfuse/langfuse](https://github.com/langfuse/langfuse) | 보안, 평가, 관측성, 품질 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 139 | [promptfoo/promptfoo](https://github.com/promptfoo/promptfoo) | 보안, 평가, 관측성, 품질 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 140 | [millionco/react-doctor](https://github.com/millionco/react-doctor) | 보안, 평가, 관측성, 품질 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 141 | [robinebers/openusage](https://github.com/robinebers/openusage) | 보안, 평가, 관측성, 품질 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 142 | [tobilg/ai-observer](https://github.com/tobilg/ai-observer) | 보안, 평가, 관측성, 품질 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 143 | [requestly/requestly](https://github.com/requestly/requestly) | 보안, 평가, 관측성, 품질 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 144 | [tiagozip/cap](https://github.com/tiagozip/cap) | 보안, 평가, 관측성, 품질 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 145 | [facebookresearch/ProgramBench](https://github.com/facebookresearch/ProgramBench) | 학습, 연구, Awesome 목록, 참고자료 | 검토 | 보안, 평가, 관측성, 품질도 가능 - 언어 모델 평가 벤치마크지만 연구 성격이 강해 현재 학습/연구 카테고리도 맞다. |
| 146 | [codecrafters-io/build-your-own-x](https://github.com/codecrafters-io/build-your-own-x) | 학습, 연구, Awesome 목록, 참고자료 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 147 | [donnemartin/system-design-primer](https://github.com/donnemartin/system-design-primer) | 학습, 연구, Awesome 목록, 참고자료 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 148 | [microsoft/PhiCookBook](https://github.com/microsoft/PhiCookBook) | 학습, 연구, Awesome 목록, 참고자료 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 149 | [microsoft/generative-ai-for-beginners](https://github.com/microsoft/generative-ai-for-beginners) | 학습, 연구, Awesome 목록, 참고자료 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 150 | [shareAI-lab/learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) | 학습, 연구, Awesome 목록, 참고자료 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 151 | [mlabonne/llm-course](https://github.com/mlabonne/llm-course) | 학습, 연구, Awesome 목록, 참고자료 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 152 | [public-apis/public-apis](https://github.com/public-apis/public-apis) | 학습, 연구, Awesome 목록, 참고자료 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 153 | [addyosmani/gemini-cli-tips](https://github.com/addyosmani/gemini-cli-tips) | 학습, 연구, Awesome 목록, 참고자료 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 154 | [Genymobile/scrcpy](https://github.com/Genymobile/scrcpy) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 155 | [OpenCut-app/OpenCut](https://github.com/OpenCut-app/OpenCut) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 156 | [vercel-labs/zero-native](https://github.com/vercel-labs/zero-native) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 157 | [microsoft/VibeVoice](https://github.com/microsoft/VibeVoice) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 158 | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 159 | [siddharthvaddem/openscreen](https://github.com/siddharthvaddem/openscreen) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 160 | [chrisryugj/kordoc](https://github.com/chrisryugj/kordoc) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 검토 | MCP, 브라우저/데스크톱 자동화, 에이전트 도구도 가능 - 문서 파서 CLI + MCP 서버라 에이전트 도구로도 볼 수 있다. HWP/PDF/Office 변환 유틸리티라 현 미디어/유틸 위치도 적합하다. |
| 161 | [hacksider/Deep-Live-Cam](https://github.com/hacksider/Deep-Live-Cam) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 162 | [Glass-HQ/Glass](https://github.com/Glass-HQ/Glass) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 163 | [automazeio/vibeproxy](https://github.com/automazeio/vibeproxy) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 164 | [manaflow-ai/cmux](https://github.com/manaflow-ai/cmux) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 165 | [remotion-dev/remotion](https://github.com/remotion-dev/remotion) | 네이티브, 미디어, 모바일/데스크톱 유틸리티 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 166 | [legalize-kr/legalize-kr](https://github.com/legalize-kr/legalize-kr) | 법률, 금융, 크립토, 기타 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 167 | [TauricResearch/TradingAgents](https://github.com/TauricResearch/TradingAgents) | 법률, 금융, 크립토, 기타 | 검토 | 멀티 에이전트 프레임워크와 플랫폼도 가능 - 멀티 에이전트 프레임워크이지만 금융 트레이딩 도메인이 핵심이라 현재 법률/금융/크립토 도메인 카테고리 유지가 낫다. |
| 168 | [virattt/ai-hedge-fund](https://github.com/virattt/ai-hedge-fund) | 법률, 금융, 크립토, 기타 | 검토 | 멀티 에이전트 프레임워크와 플랫폼도 가능 - AI 에이전트 팀 구조지만 헤지펀드/투자 의사결정 도메인이 핵심이라 현재 금융 카테고리 유지가 낫다. |
| 169 | [dabit3/x402-starter-kit](https://github.com/dabit3/x402-starter-kit) | 법률, 금융, 크립토, 기타 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 170 | [Dhaiwat10/x402-sovereign](https://github.com/Dhaiwat10/x402-sovereign) | 법률, 금융, 크립토, 기타 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 171 | [jlevy/og-equity-compensation](https://github.com/jlevy/og-equity-compensation) | 법률, 금융, 크립토, 기타 | 유지 | 현재 카테고리가 주된 가치와 맞음 |
| 172 | [wevm/wagmi](https://github.com/wevm/wagmi) | 법률, 금융, 크립토, 기타 | 유지 | 현재 카테고리가 주된 가치와 맞음 |

## 주요 출처

- GitHub GraphQL/API: 전체 172개 레포의 description, topics, primary language, stars, pushedAt, fork/archive 여부
- [anthropics/claude-code-action](https://github.com/anthropics/claude-code-action)
- [davebcn87/pi-autoresearch](https://github.com/davebcn87/pi-autoresearch)
- [understudy-ai/understudy](https://github.com/understudy-ai/understudy)
- [nibzard/awesome-agentic-patterns](https://github.com/nibzard/awesome-agentic-patterns)
- [msitarzewski/agency-agents](https://github.com/msitarzewski/agency-agents)
- [TanStack CLI docs](https://tanstack.com/cli/latest)
- [cloudflare/telescope](https://github.com/cloudflare/telescope)
- [T3 Code](https://t3.codes/)
