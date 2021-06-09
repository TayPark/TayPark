## 박태형(Tay Park)
- 과학기술정보통신부, 한국정보산업연합회 산하 소프트웨어 마에스트로 12기 연수생
- 주니어 백엔드 개발자
- 백엔드, 인프라에 관심
- 스킬
  - `Node.js`
  - `JavaScript` and `TypeScript`
  - `Java`
  - `Docker`
  - `mongoDB`
  - `MySQL`
  - `AWS`
    - `EC2`
    - `S3`
    - `CodePipeline`
    - `Lambda`

---

반갑습니다! **도메인과 요구사항에 바르게 집중하자**라는 모토로 개발하는 **TayPark** 입니다. 이는 아래의 의미입니다.

1. 주어진 도메인 내에서
2. 요구사항에 대한 배경을 이해하고 
3. 내가 해야할 일을 정확하게 파악하여 진행하고
4. 그것을 온전히 내 것으로 만드는 것입니다.

여러 사람을 만나면서 서로의 어두운 인사이트를 밝혀주는 미팅을 좋아합니다. 잘 부탁드립니다.

## 작업

**2021.02 ~ [오픈 만화번역 SNS 프로젝트](http://www.epiclogue.com) 의 타입스크립트 마이그레이션**

- TypeScript 4.0.0+ 마이그레이션
- TDD도입과 기존 테스트 케이스 강화
- 로깅 방식 개편(log rotation)
- Repository pattern, DI pattern 도입

---

**2020.03 ~ [오픈 만화번역 SNS 프로젝트](http://www.epiclogue.com) 와 [문서화](https://api.epiclogue.com/api-docs) 및 유지보수**

- Node.js 백엔드 개발
    - (2020) HTTP API 설계, 리팩토링, 로깅 고도화, 아키텍처 설계
    - (2020) 테스트 도입(Jest), 인증(JWT)
    - (2021) 테스트 타겟 DB를 Real DB Test Table에서 Memory DB로 변경
    - (2021) 캐시서버 `Redis` 도입
    - (2021) FE서버 NextJS dockerizing과 AWS CodePipeline 개편
    - (2021)`pm2`기반 클러스터링 도입
    - (2021) 로깅 방식 개편(rotation)과 풍부한 로그 제공
- MongoDB
    - (2020) 스키마 설계, 이중화, 트랜잭션 도입
- Docker(-compose)
    - Frontend: Nginx, NextJS Dockerizing
    - Backend: Nginx, Express(Cluster), MongoDB, Redis Dockerizing
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
- [서버](https://github.com/chisacam/dbeacon_api)와 통신, 데이터에 맞게 렌더링
