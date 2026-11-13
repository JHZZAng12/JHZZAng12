# JHZZAng12

## Backend & Systems Automation

백엔드 개발과 시스템 자동화에 관심이 있습니다. 요청 로그를 수집·분석하는 관제 시스템과 반복 Git 작업을 자동화하는 도구를 만들었습니다.

## Featured Projects

- **SelDi** — 사진과 증상에서 AI가 단서를 추출하고, 규칙 엔진이 고장 원인 후보를 좁힙니다. `Next.js` · `FastAPI` · `PostgreSQL` · [시연](https://seldi-fresh-frontend.vercel.app/)
- **웹서비스 장애 관제** — API 요청 로그와 사용자 제보를 함께 보고, Hadoop 집계부터 Oracle 저장까지 자동화했습니다. `Spring Boot` · `Hadoop` · `Oracle` · [시연 영상](https://youtu.be/CIOXdKjb7LM)
- **계약안심** — PDF에서 위험 조항 후보를 찾고, AI가 제시한 근거를 계약서 원문과 대조합니다. `Next.js` · `TypeScript` · `Supabase` · [시연](https://youth-housing-risk-ai-frontend.vercel.app/)
- **Git Auto Backup** — Python 파일 변경을 감지해 자동으로 커밋하고, 푸시에 실패하면 재시도합니다. `Python` · `Git` · [코드](https://github.com/JHZZAng12/git-auto-backup)

![웹서비스 장애 관제 대시보드의 로그 분석 결과와 API별 오류율](assets/monitoring-dashboard.png)

## Automation

- **웹서비스 장애 관제** — 대시보드에서 분석 버튼을 누르면 로그 전송, HDFS 업로드, MapReduce 집계, Oracle 저장, 화면 갱신이 차례로 실행됩니다.
- **Git Auto Backup** — 2초마다 Python 파일의 변경을 확인합니다. 마지막 변경 후 30초 동안 추가 변경이 없으면 자동으로 커밋하고, 푸시가 실패하면 30초 간격으로 재시도합니다.
- **계약안심** — main 브랜치에 변경을 올리거나 main을 대상으로 PR을 열면 GitHub Actions가 Vitest, 빌드, 타입 검사, Playwright를 실행하도록 설정했습니다.

## AI-Assisted Development

- **SelDi** — Codex에 진단 이력 저장 과정을 점검하도록 요청했습니다. 결과 화면에서 증상 텍스트가 빠져 API가 422를 반환하는 조건을 재현했습니다. 증상 텍스트를 요청에 유지하도록 보완한 뒤, 같은 조건에서 진단과 이력 저장이 성공하는지 다시 확인했습니다.
- **계약안심** — AI 코드 리뷰 후 시연용 PDF로 다시 확인하는 과정에서, PDF 헤더가 첫 조항에 붙어 같은 조항이 중복 집계되는 문제를 찾았습니다. 조항 번호를 기준으로 본문을 나누고, 번호 표기가 달라도 본문이 같으면 같은 근거로 처리하도록 수정했습니다. 두 경우를 회귀 테스트로 남겼습니다.

## Education & Certifications

- 대전대학교 컴퓨터공학과
- HRD 빅데이터 기반 AI 물류 자동화 시스템 개발 과정
- 초경량비행장치 조종자(1종)

[개인 홈페이지](https://jhzzang12.github.io/)
