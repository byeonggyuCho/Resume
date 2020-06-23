# Admin Web
2019.05~2019.06

## TL;DR
- 구글 OTP를 이용한 로그인처리
- Oracle 쿼리 짜기
- 화면 스크립트 로직 개발.
- DB 마이그레이션 Mysql -> Oracle



## intro
보험 설계사가 태블릿으로 영업하는 채권앱에 대한 관리자 페이지입니다.  
인스웨이브에서 제공하는 WRM(WebSpuare Reference Model, 어드민 템플릿 프로젝트) 기반으로 고객 요구사항에 맞추어 개발했고 DB 설계를 제외한 전과정을 수행했습니다.  
UI변경사항이 많지 않았고 주된 작업은 DB마이그레이션 작업이 가장 많은 시간이 걸렸습니다.  


## 작업내용
DB설계를 제외한 풀스택
- 프론트(퍼블리싱, 스크립트)
- Spring기반의 Rest API 구현



##  Skill
- Websquare
- ES5 with Promise
- Oracle
- Spring
- Google OTP를 활용한 로그인 서비스

## 개발후기
- 그리드에 중점적인 Servcie로 상황별 이벤트처리를 꼼꼼히 하는것이 어려웠음.
- Query를 짜는 연습을 많이함.
- 첫 화면 개발 이후 하위 메뉴는 거의다 비슷한 grid구조이기 때문에 큰 어려움은 없었음.
- 공통로직을 직접 처리하면서 각 업무화면 소스를 깔끔하게 정리되는 걸 경험함.
    - e.g. com.groupByJSON (at common.js)
    - e.g. getDiffDateToString (at. Util.java)
- admin이다 보니 각 메뉴별 연계되는 부분에서 logic오류가 발생함.
    - 사용자에게 권한을 부여했는데 다른 탭에서 적용이 안되어 ReLoad를 해야하는 상황 발생.
    - 공통 코드르 추가했는데 다른 페이지에서 조회가 안됨
    - 다른 사용자에게 권한을 부여할 수 있는 Super Admin에 대한 처리
- Login 로직을 많이 고민함.
    - 비밀번호 만료
    - 비밀번호 암호화
    - 장기 미접속 검증
    - 사용자별 권한 체크 인터셉터.
    - 초기 비밀번호 접속시 Logic처리.
- 기본적인 게시판 연습이 많이 됨.