# Key-Catch - 키워드 기반 정보 구독 및 알림 서비스

사용자가 설정한 키워드를 기반으로 외부 사이트의 정보를 주기적으로 수집하고,
새로운 정보가 발견되면 이메일 알림을 제공하는 서비스입니다.

본 시스템은 Spring Boot 기반 3-Tier Architecture로 설계되었으며,
API 서버와 백그라운드 작업(Crawler, Notification Worker)을 분리하여
사용자 요청 처리와 데이터 수집/알림 작업을 독립적으로 수행하도록 구성했습니다.

- **Presentation Tier** : Frontend (Vercel)
- **Application Tier** : Spring Boot API Server, Crawler, Notification Worker
- **Data Tier** : MySQL

이를 통해 사용자 요청 처리와 크롤링/알림 작업 간의 성능 영향을 최소화하고
확장 가능한 구조를 목표로 설계했습니다.

<br>

## 시스템 아키텍처

<img src="./assets/architecture.png" width="800">

<br>

## 🚀 Service Components
각 서비스명을 클릭하면 해당 레포지토리의 상세 기술 명세로 이동합니다.

| 서비스 구분 | 레포지토리 링크 | 핵심 역할 |
| :--- | :--- | :--- |
| **Main API** | [🔗 project-api-server](https://github.com/NotiLink/project-api-server) | 비즈니스 로직 및 사용자/키워드 관리 |
| **Notifier** | [🔗 project-notifier](https://github.com/NotiLink/project-notifier) | 1분 단위 스케줄링 및 메일 발송 |
| **Crawler** | [🔗 project-crawler](https://github.com/NotiLink/project-crawler) | 외부 사이트 데이터 수집 및 파싱 |
| **Frontend** | [🔗 project-frontend](https://github.com/NotiLink/project-frontend) | 유저 구독 설정 UI (Vercel 배포) |

<br>

