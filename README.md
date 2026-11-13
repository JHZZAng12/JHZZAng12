# JHZZAng12

**Backend & Systems Automation**

## Featured Projects

| 프로젝트 | 주요 기능 | 링크 |
| --- | --- | --- |
| **웹서비스 장애 관제** | API별 요청 수와 오류율을 대시보드에 표시하고, 사용자 제보를 함께 보여줍니다. `Spring Boot` · `Hadoop` · `Oracle` | [시연 영상](https://youtu.be/CIOXdKjb7LM) |
| **SelDi** | 제품 사진과 증상을 입력하면 AI가 단서를 찾고, 진단 규칙에 따라 고장 원인 후보와 조치 방법을 안내합니다. `Next.js` · `FastAPI` · `PostgreSQL` | [서비스 보기](https://seldi-fresh-frontend.vercel.app/) |
| **계약안심** | 계약서 PDF에서 주의할 조항을 찾아 원문 인용과 함께 보여줍니다. `Next.js` · `TypeScript` · `Supabase` | [서비스 보기](https://youth-housing-risk-ai-frontend.vercel.app/) |
| **Git Auto Backup** | 작업 중에 바뀐 Python 파일을 GitHub에 자동으로 백업합니다. `Python` · `Git` | [코드 보기](https://github.com/JHZZAng12/git-auto-backup) |

![웹서비스 장애 관제 대시보드에 표시된 API별 오류율](assets/monitoring-dashboard.png)

## Automation

- **웹서비스 장애 관제** — 대시보드에서 분석 버튼을 누르면 HDFS로 로그를 보내고, MapReduce로 집계해 Oracle에 저장합니다. 저장이 끝나면 대시보드에 새 결과가 표시됩니다.
- **Git Auto Backup** — Python 파일을 2초마다 확인합니다. 30초 동안 추가 변경이 없으면 커밋하고 GitHub에 올립니다. 푸시에 실패하면 30초 뒤 다시 시도합니다.
- **계약안심** — `main`에 변경을 푸시하거나 `main`으로 PR을 보내면 GitHub Actions에서 Vitest, 빌드, 타입 검사, Playwright 브라우저 테스트가 차례로 실행됩니다.

## AI-Assisted Development

- **SelDi** — Codex와 진단 요청을 따라가 보니, 결과 화면에서 증상 내용이 빠질 때 API가 422 오류를 반환하고 이력이 저장되지 않았습니다. 증상이 요청에 포함되도록 고친 뒤, 같은 조건에서 진단 결과가 나오고 이력도 저장되는지 확인했습니다.
- **계약안심** — AI 코드 리뷰 뒤 예제 PDF를 다시 분석하다가 같은 조항이 두 번 집계되는 문제를 찾았습니다. PDF 제목이 첫 조항에 붙어 들어오는 경우를 처리하고, 조항 번호를 뺀 인용 문구가 같으면 한 번만 집계하도록 고쳤습니다. 두 경우를 각각 테스트로 남겼고, 로컬에서 모두 통과했습니다.

## Education & Certifications

- 대전대학교 컴퓨터공학과
- HRD 빅데이터 기반 AI 물류 자동화 시스템 개발 과정
- 초경량비행장치 조종자(1종)

[개인 홈페이지](https://jhzzang12.github.io/)
