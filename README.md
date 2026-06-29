# 🏆 경산시 관광 웹 서비스 프로젝트

> 제1회 교내 SW중심대학 융합그룹 실무 경진대회 우수상 수상작

<br>

## 📌 프로젝트 개요

경산시 관광 정보를 제공하고, 사용자가 자신만의 여행 코스를 계획하고 관리할 수 있도록 돕는 웹 서비스입니다.

| 항목 | 내용 |
|------|------|
| 📅 진행 기간 | 2025 |
| 👥 팀 구성 | 팀 프로젝트 |
| 🏆 수상 | 제1회 교내 SW중심대학 융합그룹 실무 경진대회 우수상 |
| 🔗 GitHub | [swproject](https://github.com/SB135246/swproject) |

<br>

## 🛠️ 기술 스택

- **백엔드:** Java 17, Spring Boot (3.5.5), Spring Data JPA, Spring Security, QueryDSL
- **프론트엔드:** HTML, CSS, JavaScript, Thymeleaf
- **데이터베이스:** MySQL
- **빌드 도구:** Gradle
- **버전 관리:** Git & GitHub

<br>

## ✨ 주요 기능

- **사용자 관리:** 다단계 회원가입 프로세스를 통해 사용자를 등록하고, 로그인 기능을 제공합니다.
- **여행 코스 생성:** 출발지, 여행 기간, 선호 장소 등을 단계별로 입력하여 맞춤형 여행 코스를 생성할 수 있습니다.
- **장소 추천:** 사용자의 취향과 선택에 기반하여 새로운 장소를 추천합니다.
- **코스 관리:** 생성된 여행 코스를 조회, 상세 확인, 삭제할 수 있습니다.
- **장소 좋아요 기능:** 관심 있는 장소에 좋아요를 표시하고, 이를 코스 생성 시 활용할 수 있습니다.
- **월간 매거진:** 큐레이션된 여행 콘텐츠를 제공합니다.
- **신고 기능:** 부적절한 콘텐츠에 대한 신고 기능을 제공합니다.
- **관광지 검색 및 필터링:** 카테고리별 관광지 조회
- **관광지 상세 정보 확인:** 사진, 설명, 위치 등

<br>

## 👨‍💻 담당 역할 (서상범)

- **좋아요(찜) 기능 구현** — LikeService, LikeController 개발, 찜한 명소 조회 및 카테고리별 분류
- **월간 매거진 기능 구현** — 매거진 컨트롤러 분리, 매거진 상세 페이지 개발
- **장소 검색 기능 구현** — 장소 검색 Service, Controller 개발
- **리뷰 기능 구현** — 리뷰 Service, Controller 개발, 별점 평균 기능 추가
- **신고 기능 구현** — ReportService, ReportController 개발
- **문의 기능 구현** — 문의 Service, Controller 개발
- **Spring Security 설정** — SecurityConfig 구성
- **여행 코스 UI 개발** — 코스짜기 화면 구현 및 기능 연동
- **홈 화면 개발** — 홈 UI 및 기능 구현

<br>

## 🏗️ 아키텍처

프로젝트는 표준 Spring Boot 계층형 아키텍처를 따릅니다.

- `controller`: 웹 요청 처리 및 UI 상호작용
- `service`: 핵심 비즈니스 로직
- `repository`: 데이터베이스 연동 (Spring Data JPA)
- `domain`: 핵심 데이터 모델 (JPA 엔티티)
- `dto`: 계층 간 데이터 전송 객체

<br>

## ▶️ 실행 방법

### 1. 필수 설치 항목
- Java 17
- Gradle
- MySQL 8.0 이상

### 2. 데이터베이스 설정

`src/main/resources/application.properties` 파일에서 MySQL 연결 정보를 설정합니다.

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/testdb?useSSL=false&serverTimezone=UTC&allowPublicKeyRetrieval=true&characterEncoding=UTF-8
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.hibernate.ddl-auto=update
```

### 3. 빌드 및 실행

```bash
./gradlew build
java -jar build/libs/swproject-0.0.1-SNAPSHOT.jar
```

또는

```bash
./gradlew bootRun
```

### 4. 접속
`http://localhost:8080`
