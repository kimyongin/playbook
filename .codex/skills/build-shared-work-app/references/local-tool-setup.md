# 에이전트가 사용하는 개발 도구

도구를 준비하는 목적은 에이전트가 설치·실행·검사·배포를 직접 처리하게 하는 것이다. 운영체제와 기존 환경을 확인하고 현재 작업에 필요한 도구를 설치해 실제 실행까지 확인한다. 사용자는 본인 인증·운영체제 승인 등 직접 행동이 필요한 순간에 참여한다.

| 도구 | 쓰임 |
| --- | --- |
| Git | 변경 이력과 작업 관리 |
| Node.js·npm | 웹 앱과 개발 패키지 실행 |
| Docker 등 컨테이너 실행 도구 | 로컬 Supabase 서비스 실행 |
| Supabase CLI | 로컬 DB·마이그레이션·서버 함수·배포 관리 |
| Deno | 서버 함수 개발과 검사 |
| Playwright와 브라우저 | 웹에서 실제 입력·클릭 흐름 확인 |
| GitHub CLI | GitHub 저장소·PR·자동화 상태 관리 |

완성된 앱의 이용자는 웹이나 에이전트로 접속한다. 위 도구들은 앱을 만드는 환경에 필요하며, 서비스 이용자의 로그인·MCP 연결과 개발자의 관리 계정 연결은 별개다.

## 환경에 맞춰 준비하기

기존 프로젝트의 버전과 설치 방식을 우선 활용한다. 새 프로젝트는 Supabase CLI와 웹 라이브러리를 프로젝트 의존성으로 관리하고 lockfile을 남기면 재현하기 쉽다. Supabase CLI는 `npx supabase`로 실행하는 구성을 기본으로 삼을 수 있다.

설치·명령·지원 버전은 실행 시 공식 안내와 설치된 도구의 도움말로 확인한다. 준비 상태와 막힌 항목은 프로젝트 시작 문서에 짧게 기록해 다음 작업에서 활용한다. 환경 제약이 있다면 가능한 연결 도구나 대안을 검토하고, 사람의 조치가 필요한 이유와 행동을 구체적으로 안내한다.

로컬 앱도 원격 DB에 연결될 수 있으므로 변경·검사 대상은 실제 연결 설정으로 확인한다. 평소 개발 데이터를 보존하는 환경과 초기화 가능한 자동 테스트 환경을 분리한다. 인증 정보는 도구의 인증 절차와 비밀값 저장 방식을 이용하며, 브라우저에 포함되는 설정에는 관리자 키나 개인 토큰을 넣지 않는다.

## 확인처

- [Supabase CLI와 로컬 실행](https://supabase.com/docs/guides/local-development/cli/getting-started)
- [Docker Desktop](https://docs.docker.com/desktop/)
- [Node.js](https://nodejs.org/en/download)
- [Deno](https://docs.deno.com/runtime/getting_started/installation/)
- [Playwright 브라우저](https://playwright.dev/docs/browsers)
- [GitHub CLI](https://cli.github.com/manual/)
