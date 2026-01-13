# Key-Catch - 키워드 기반 정보 구독 및 알림 서비스

사용자가 설정한 키워드에 맞는 정보를 실시간으로 수집하여 알림을 제공하는 MSA 기반의 분산 시스템입니다.

<br>

## 시스템 아키텍처

<img src="./assets/architecture.png" width="800">

<br>

## 🚀 Microservices Navigator
각 서비스명을 클릭하면 해당 레포지토리의 상세 기술 명세로 이동합니다.

| 서비스 구분 | 레포지토리 링크 | 핵심 역할 |
| :--- | :--- | :--- |
| **Main API** | [🔗 project-api-server](https://github.com/NotiLink/project-api-server) | 비즈니스 로직 및 사용자/키워드 관리 |
| **Notifier** | [🔗 project-notifier](https://github.com/NotiLink/project-notifier) | 1분 단위 스케줄링 및 메일 발송 |
| **Crawler** | [🔗 project-crawler](https://github.com/NotiLink/project-crawler) | 외부 사이트 데이터 수집 및 파싱 |
| **Frontend** | [🔗 project-frontend](https://github.com/NotiLink/project-frontend) | 유저 구독 설정 UI (Vercel 배포) |

<br>

## 공통 기술 스택
