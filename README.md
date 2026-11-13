# JHZZAng12

**Backend & Systems Automation**

Spring Boot와 FastAPI로 백엔드를 개발했습니다. 서비스 로그를 모아 장애를 분석하는 시스템과 Python 파일을 GitHub에 자동으로 백업하는 도구를 만들었습니다.

[개인 홈페이지](https://jhzzang12.github.io/)

## Tech Stack

- **백엔드** · Java, Spring Boot, Python, FastAPI
- **웹** · TypeScript, Next.js
- **데이터베이스·배포** · Oracle, PostgreSQL, Supabase, Vercel
- **로그 분석·테스트** · Hadoop, GitHub Actions, Vitest, Playwright

## Core Skills

- **API 개발과 데이터 저장** — SelDi에서 사진과 증상을 받아 추가 질문과 진단 결과를 돌려주는 API를 만들었습니다. 완료된 진단은 PostgreSQL에 저장해 다시 조회할 수 있습니다.
- **로그 분석 자동화** — 장애 관제 화면에서 분석 버튼을 누르면 로그를 HDFS로 전송하고, MapReduce로 집계한 결과를 Oracle에 저장합니다. 저장이 끝나면 대시보드가 갱신됩니다.
- **테스트 자동화** — 계약안심에서 `main`에 코드가 올라오거나 PR이 열리면 GitHub Actions가 단위 테스트, 빌드, 타입 검사, 브라우저 테스트를 실행하도록 구성했습니다.
- **AI 검토와 재검증** — SelDi에서 증상 내용이 빠지면 진단 이력이 저장되지 않는 문제를 Codex와 재현하고, 수정 후 같은 요청 흐름에서 저장을 확인했습니다. 계약안심에서는 AI 코드 리뷰 뒤 예제 PDF를 다시 분석해 조항이 중복 집계되는 문제를 찾았습니다. 조항을 나누는 방식과 중복 판정 기준을 고친 뒤 회귀 테스트 2개가 통과했습니다.

## Featured Projects

| 프로젝트 | 주요 기능 | 링크 |
| --- | --- | --- |
| **웹서비스 장애 관제** | API별 요청 수와 오류율, 사용자 제보를 한 화면에서 확인할 수 있습니다. | [시연 영상](https://youtu.be/CIOXdKjb7LM) |
| **SelDi** | 제품 사진과 증상을 입력하면 AI가 단서를 찾고, 진단 규칙에 따라 고장 원인 후보와 조치 방법을 안내합니다. | [서비스 보기](https://seldi-fresh-frontend.vercel.app/) |
| **계약안심** | 계약서 PDF에서 주의할 조항을 찾아 원문을 인용해 보여줍니다. | [서비스 보기](https://youth-housing-risk-ai-frontend.vercel.app/) |
| **Arduino 거리 기반 모터 제어** | PIR 센서가 움직임을 감지하면 초음파로 거리를 재고, 거리 구간에 따라 모터 PWM과 경고 LED를 제어하는 시제품입니다. | [시연 영상](https://youtu.be/Ds1BTGLDAUU) |

## Developer Tools

| 도구 | 주요 기능 | 링크 |
| --- | --- | --- |
| **Git Auto Backup** | Python 파일이 바뀐 뒤 30초 동안 추가 변경이 없으면 커밋하고 GitHub에 올립니다. 푸시에 실패하면 30초 간격으로 다시 시도합니다. | [GitHub](https://github.com/JHZZAng12/git-auto-backup) |

## Education & Certifications

- 대전대학교 컴퓨터공학과
- HRD 빅데이터 기반 AI 물류 자동화 시스템 개발 과정
- 초경량비행장치 조종자(1종)
