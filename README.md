## 박태형(Tay Park)
- (2021) 과학기술정보통신부, 한국정보산업연합회 산하 **소프트웨어 마에스트로 12기 연수생**
- 주니어 백엔드 개발자
- 백엔드, 인프라, 데이터에 관심
- 스킬
  - `Node.js`, `JavaScript(ES6)` and `TypeScript`
  - `Java`
  - `Docker`
  - `mongoDB`
  - `MySQL`
  - `AWS`
    - `EC2`
    - `S3`
    - `CodePipeline`
    - `Lambda`
    - `SNS`

---

반갑습니다! **도메인과 요구사항에 바르게 집중하자**라는 모토로 개발하는 **TayPark** 입니다. 이는 아래의 의미입니다.

1. 주어진 도메인 내에서
2. 요구사항에 대한 배경을 이해하고 
3. 내가 해야할 일을 정확하게 파악하여 진행하고
4. 그것을 온전히 내 것으로 만드는 것입니다.

여러 사람을 만나며 서로의 어두운 부분을 밝혀주는 대화을 좋아합니다. 잘 부탁드립니다.

## 작업

**2021.07 ~  [Spark+ DB updater](https://github.com/SWM-SparkPlus/db-updater) 개발 및 유지보수**
- [Spark+](https://github.com/SWM-SparkPlus)는 [Apache Spark](https://spark.apache.org/)에서 한국 주소체계 데이터와 위치정보 데이터의 효율적인 처리를 위한 pyspark 패키지 개발하는 프로젝트
  - 프로젝트 기획, 개발, 문서화
  - `TypeScript`, `Node.js`, `MySQL`, `Prisma`, `TypeORM`, `Docker`, `Shell` 사용
  - `db-updater`는 네트워크를 통한 도로명주소 API가 아닌 빅데이터 엔진인 Spark에서 데이터 지역성의 확보로 더 빠른 데이터 참조를 돕는 데이터베이스를 통합하여 구축하고 매일 최신화하는 컴포넌트
  - [도로명주소 홈페이지](https://www.juso.go.kr/addrlink/addressBuildDevNew.do?menu=match)로 부터 최신 전체 데이터 다운로드(월별) 및 일일 데이터베이스 동기화 스크립트 개발
  - `Prisma` model push를 이용한 데이터베이스 정의
  - `MySQL` 시스템 변수 파일인 **my.cnf**에 대한 이해와 로깅을 이용한 디버깅, 성능 튜닝 경험(프로세스 및 커넥션 수, 로그 명시, 글로벌 변수 관리)
    - Node.js의 특징인 비동기 처리를 최대한 활용하기 위해 MySQL 프로세스 수 모니터링 및 성능 튜닝
  - 데이터베이스 테이블 구축 프로세스 최적화 경험
    - 최초 4개의 통합 테이블 설계(전체 데이터 2000만건), 구축 시간 50분 소요
    - 17개 광역자치시로 테이블 분리, 25분으로 감소
    - Process spawning을 이용하여 멀티 프로세싱 작업으로 전환, 12분으로 감소
    - ARM64아키텍처(M1 Macbook Air)에서 AMD64 아키텍처로 머신 아키텍처 변경. 최대 1분까지 단축 경험(36 vCPUs, 72G RAM) [영상](https://www.youtube.com/watch?v=A-lPvNXl8bs&ab_channel=TayPark)
  - `TypeORM`을 이용한 Dynamic query 수행(일일 업데이트)
    - 4개의 동일한 스키마를 공유하는 17개의 테이블이 존재(총 68개)
    - 테이블 이름만 다르므로 같은 Entity를 갖는 테이블에 대해 테이블명을 주입받아 메타데이터를 연결한 커넥션에 업데이트하고 쿼리 수행
    - 하지만 비효율성과 성능 문제로 raw query로 전환
  - Docker image와 명령어 아키텍처에 대한 이해
    - MySQL 8.0.26 기준 arm64/v8 이미지가 존재하지 않음(Supported architectures: amd64)
    - 해당 이미지를 M1 맥북에서 실행했을 때와 인텔 CPU에서 실행했을 때 성능 차이 경험(경우에 따라 5~10배)
    - 성능 최적화에 포커스를 맞춰 AWS 인스턴스, M1맥북, 인텔CPU 노트북에서 지속적으로 테스트 실행.
  - GitLab과 GitHub 동시 관리
  - AWS 인스턴스 관리
    - EC2 개발서버 및 데이터베이스 서버 운용
    - 이벤트 소싱을 위한 SNS, 수신하여 Slack 메세지를 보내는 Lambda 
  - [한글 및 영어 문서화, 위키 작성](https://github.com/SWM-SparkPlus/db-updater/wiki)

---

**2021.02 ~ [오픈 만화번역 SNS 프로젝트](http://www.epiclogue.com) 의 타입스크립트 마이그레이션**

- TypeScript 4.x 마이그레이션
- TDD도입과 기존 테스트 케이스 강화
- 로깅 방식 개편(rich log, log rotation)
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
