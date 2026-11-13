# JHZZAng12

**Backend & Systems Automation**

서비스 장애를 살펴볼 수 있는 관제 시스템과 반복되는 Git 작업을 줄이는 도구를 만들었습니다. AI가 짚은 문제는 먼저 재현해 보고, 수정한 뒤 같은 조건에서 다시 확인합니다.

## Featured Projects

| 프로젝트 | 주요 기능 | 링크 |
| --- | --- | --- |
| **웹서비스 장애 관제** | API 요청 로그와 사용자 제보를 바탕으로 장애 여부를 판단합니다. Hadoop으로 로그를 집계해 Oracle에 저장합니다. `Spring Boot` · `Hadoop` · `Oracle` | [시연 영상](https://youtu.be/CIOXdKjb7LM) |
| **SelDi** | 제품 사진과 증상을 입력하면 AI가 단서를 찾고, 규칙 엔진이 가능한 고장 원인을 좁혀 줍니다. `Next.js` · `FastAPI` · `PostgreSQL` | [서비스 보기](https://seldi-fresh-frontend.vercel.app/) |
| **계약안심** | 계약서 PDF에서 주의할 조항을 찾고, AI가 인용한 문구가 원문에 있는지 확인합니다. `Next.js` · `TypeScript` · `Supabase` | [서비스 보기](https://youth-housing-risk-ai-frontend.vercel.app/) |
| **Git Auto Backup** | Python 파일이 바뀌면 자동으로 커밋하고, 푸시가 실패하면 다시 시도합니다. `Python` · `Git` | [코드 보기](https://github.com/JHZZAng12/git-auto-backup) |

![웹서비스 장애 관제 대시보드에 표시된 API별 오류율](assets/monitoring-dashboard.png)

## Automation

- **웹서비스 장애 관제** — 분석 버튼을 한 번 누르면 로그를 HDFS로 보내고, MapReduce로 집계한 결과를 Oracle에 저장한 뒤 대시보드를 갱신합니다.
- **Git Auto Backup** — 2초마다 파일 변경을 확인합니다. 마지막 변경으로부터 30초가 지나면 커밋하고, 푸시에 실패하면 30초마다 다시 시도합니다.
- **계약안심** — `main`에 코드를 올리거나 병합을 요청하면 GitHub Actions에서 Vitest 테스트, 빌드, 타입 검사, Playwright 브라우저 테스트가 차례로 실행되도록 설정했습니다.

## AI-Assisted Development

- **SelDi** — Codex와 진단 이력이 저장되지 않는 경우를 살펴봤습니다. 결과 화면에서 증상이 빠진 채 요청을 보내면 API가 422 오류를 반환했습니다. 요청에 증상이 빠지지 않도록 고친 뒤, 같은 조건에서 진단 결과가 나오고 이력도 저장되는지 확인했습니다.
- **계약안심** — AI 코드 리뷰를 마친 뒤 예제 PDF로 다시 점검하다가, 제목과 첫 조항이 붙어 추출되면서 같은 조항이 두 번 집계되는 문제를 발견했습니다. 조항 번호를 기준으로 본문을 나누고, 번호가 있든 없든 본문이 같으면 한 번만 집계하도록 고쳤습니다. 관련 회귀 테스트 2개를 로컬에서 실행해 통과를 확인했습니다.

## Education & Certifications

- 대전대학교 컴퓨터공학과
- HRD 빅데이터 기반 AI 물류 자동화 시스템 개발 과정
- 초경량비행장치 조종자(1종)

[개인 홈페이지](https://jhzzang12.github.io/)
