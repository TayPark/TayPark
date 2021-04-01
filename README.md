## Taypark
- South Korea
- Backend developer, Infra engineer
- Always be curious on newer techs
- Tech stacks: 
  - `Node.js + ES6`, `Java`, `Android`, `MongoDB`, `MySQL`, `AWS`

> 요구사항와 비즈니스 로직에 바르게 집중하자라는 모토로 개발하는 **taypark** 입니다. 정확한 비즈니스 요구사항 파악으로 협업을 도모하며 업무의 자동화를 통해 개발 생산성을 높이는 일을 하고 싶습니다.

## Works

**2021.02 ~ [오픈 만화번역 SNS 프로젝트](http://www.epiclogue.com) 의 타입스크립트 마이그레이션**

- TypeScript 4.0.0+ 마이그레이션
- TDD도입과 테스트 케이스 강화
- 로깅 방식 개편(log rotation)
- Repository pattern, DI pattern 도입
- 환경변수파일을 기반으로 한 철저한 환경 분리

---

**2020.03 ~ [오픈 만화번역 SNS 프로젝트](http://www.epiclogue.com) 와 [문서화](https://api.epiclogue.com/api-docs) 및 유지보수**

- Node.js 백엔드 개발
    - HTTP API 설계, 리팩토링, 로깅 고도화
    - 테스트 도입(Jest), 인증(JWT), API 문서화(Swagger UI)
    - (2021) 테스트 타겟 DB를 Real DB Test Table에서 Memory DB로 변경
- MongoDB
    - 스키마 설계, 이중화, 트랜잭션
- Docker(-compose)
    - Frontend: NextJS, Nginx Dockerizing
    - Backend: Nginx, Express, MongoDB Dockerizing
- AWS 배포
    - 애플리케이션 배포 인스턴스 EC2, 정적 파일 S3 사용
    - 배포 자동화를 위한 CodePipeline 도입(+CodeBuild, CodeDeploy)
        - Slack webhook과 AWS Lambda 연동
        - 프론트엔드 서버 구조 변경으로 인한 NextJS서버 Dockerizing 및 CodePipeline 유지보수

---

**2020.11 ~ 2020.12 [안드로이드 앱](https://github.com/TayPark/mp-stil-android), [서버](https://github.com/TayPark/mp-stil-server) 개발 (학부 과제)**

- 요구사항 설계 및 구현
- 안드로이드(Java)
    - 서버와 통신하고 데이터에 따라 렌더링
- 서버
    - Node.js API 서버
    - MongoDB

---

**2020.08 ~ 2020.09 [REST API 구현](https://github.com/TayPark/node-rest-api) (오픈 만화번역 SNS 프로젝트의 기반 설계)**

- Node.js 백엔드 개발
- Database
    - 캐싱(Redis)
    - MySQL + Sequelize(ORM)
- Error reporting
    - Sentry

---

**2020.04 ~ 2020.05  [React Native 근태관리 App](https://github.com/TayPark/dbeacon) 개발 (졸업작품)**

- React Native (React 16) 앱 UI 및 기능 개발
- [서버](https://github.com/TayPark/dbeacon_api)와 통신, 데이터에 맞게 렌더링
