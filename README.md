# Today I Learned (TIL)
https://github.com/JinYunhwa/TIL

## C

## Java

## [lecture](./lecture/)
## vue.js
 + [테스트](./vue.js/test.md)

## Database
 + []


## commit 규칙
type(scope) : title 
body ( 본문, 생략가능 )
footer

type
feat : 새로운 기능 추가
fix : 버그 수정, 약간의 수정사항이 있을 때
docs : 문서 수정
style : 코드 포맷, 세미콜론 누락, 코드 변경이 없는 경우
refactor : 코드 리팩토링
test : 테스트 코드, 리팩토링 테스트 코드 추가
chore : 빌드 업무 수정, 패키지 매니저 수정

title
간결하게 마침표는 붙이지 않는다.
과거시제 x
한글로 작성시 명사형종결문(~함, 쉽게말해 음슴체)
영어로 작성시 동사가 앞으로 오는 명령문 (첫글자는 대문자)
이슈번호가 있으면 붙이기

body
제목에 대한 설명이 필요할때(선택사항)
무엇을, 왜 했는지 작성

footer
Resolves : #issue, .... (해결한 이슈, 생략 가능)
See also : #issue, .... (참고 이슈, 생략 가능)
Issue Tracker ID를 작성할 때 사용

## 깃허브 레포 합치기
 1. git remote add <리모트명> <레포지토리 url>
 2. git subtree add --prefix=<폴더명> <리모트명> <부모 레포지토리의 브랜치>
 3. git push
 4. 자식 레포지토리 삭제

## reference
 https://github.com/mangdo/TIL/blob/main/Database/RDBMS-vs-NoSQL.md
 https://firstblog912.tistory.com/165
 깃허브 레포 합치기 - https://yeonyeon.tistory.com/169
 깃 커밋 로그 확인 - https://bite-sized-learning.tistory.com/198
 마크다운 언어 사용법 - https://80000coding.oopy.io/bbfbfed5-d55c-4aaf-a2b8-b52578472d0d