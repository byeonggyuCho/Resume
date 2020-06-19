# W-craft


## TL;DR
1. AST 분석
2. 파입 입출력.


## intro
UI flatform 마이그레이션 툴.


## 작업내용.
- softbase사의 Xframe 변환 로직 작성.
- 솔루션 안정화

## 상세화면

### 환경설정
![](../resource/wcraft/1.png)
1. 타겟 플렛폼 설정
2. 타겟 폴더 설정
3. 룰 셋팅.


### 분석단계
![](../resource/wcraft/2.png)
1. 변환 파일 목록 생성.
2. 매핑률 분석 (chart.js)

### 변환
![](../resource/wcraft/3.png)
1. 레이아웃 변환
2. 스크립트 변환
3. 변환 파일 병합.

### 룰 입력
![](../resource/wcraft/4.png)
1. 플랫폼별 룰 정보 추가 및 수정

### 룰 매핑 상태 확인.
![](../resource/wcraft/5.png)
- 미 매핑 룰 확인.



## 작업 후기
- 기존의 전환툴에서 PlatForm에 대한 전환룰을 작성하는것
- 기존 전환툴에 전환을 위한 Core 로직은 작성된 상황이라 큰 어려움은 없었음.
- xFrame의 Xml파일의 dom구조를 분석하여 websqure문서로 만드는것이 가장 어려웠음.
    - i.g. Grid구조에서 헤더병합이나 Grid Body 병합같은 부분.