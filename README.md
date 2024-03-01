# h2 DataBase

H2 데이터베이스는 경량 및 내장형(in-memory) 데이터베이스 시스템으로, Java로 개발된 오픈 소스 데이터베이스이므로 유닛 테스트에 적합하여 숙련도가 높이고자 공부하였습니다, 설정 코드는 위 파일에 작성되어 있습니다.

## 설정을 끝내고 h2 db 사용 방법

<img src="https://github.com/Hong5743/h2-DB/assets/136396772/611e709f-9e90-4f6f-9342-2bb3882bbd55"  width="400" height="400"/>

 - browser에서 아래 url을 접속하면 위와 같은 화면이 나타난다 (설정 정보 기반 url)
 - http://localhost:8080/h2-console

<img src="https://github.com/Hong5743/h2-DB/assets/136396772/e0386e31-4929-4a45-955a-a3810e2151d0"  width="400" height="400"/>

 - 앞에서 설정한 정보를 입력하여 로그인을 하면 위와 같은 웹 기반 콘솔이 제공됨

## 테이블 생성을 위한 DB Table 및 데이터의 초기화

### DB Table 생성
Spring 프로젝트의 resources 디렉토리 하위에 schema.sql 파일 생성 후 SQL을 작성

<img src="https://github.com/Hong5743/h2-DB/assets/136396772/e13c9559-506e-4698-ad18-3feffadebd3a"  width="400" height="400"/>

```
DROP TABLE IF EXISTS todo;

CREATE TABLE todo
(
  id INTEGER PRIMARY KEY AUTO_INCREMENT,
  content VARCHAR(25%) NOT NULL,
  isCompleted CHARACTER NOT NULL
);
```

Spring 프로젝트의 resources 디렉토리 하위에 schema.sql 파일 생성 후 SQL을 작성하면 동작하며 스키마가 생성이 된다.
<img src="https://github.com/Hong5743/h2-DB/assets/136396772/e7f1962a-affa-44b4-8fc8-5dad2ddd39bd"  width="400" height="400"/>

### 데이터 초기화

Spring 프로젝트의 resources 디렉토리 하위에 data.sql 파일 생성 후 SQL을 작성한다

<img src="https://github.com/Hong5743/h2-DB/assets/136396772/3dd6d73b-4207-4a71-a6b5-0ab7d1b417a3"  width="400" height="400"/>
<br>
<img src="https://github.com/Hong5743/h2-DB/assets/136396772/b99d00e4-b62a-4f2e-a524-8d0d0b4c2f99"  width="600" height="200"/>

Spring Boot 애플리케이션 재시작 후 H2 DB 콘솔에서 확인해보면, data.sql의 SQL문이 동작한 것을 확인할 수 있다

<img src="https://github.com/Hong5743/h2-DB/assets/136396772/25268c11-aa3c-4822-8e71-0d02831d9b8c"  width="400" height="400"/>



