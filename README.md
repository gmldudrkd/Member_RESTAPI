사용 기술 및 구현 스펙
-
- python3
- sqlite3
- flask 프레임워크
- flask-restful 모듈

로컬에서 실행 방법
-
[API test 프로그램]
- 크롬확장 프로그램 사용
- https://chrome.google.com/webstore/detail/restlet-client-rest-api-t/aejoelaoggembcahagimdiliamlcdmfm

[설치 과정]
- Python 3.0 이상 설치
- pip3 install Flask
- pip3 install flask-restful
- python create_db.py > userInfo 테이블 생성
- python app.py

API 명세서
-
- swagger로 작성한 임의 명세서 입니다.
- Base Url은 http://127.0.0.1:5000 입니다.
- https://app.swaggerhub.com/apis-docs/gmldudrkd/Ably_API/1.0.0#/

최종 구현된 범위
-
- 명확한 API 응답을 주기위해 최대한의 유효성체크를 진행하였습니다.

[사용자 회원가입]
- 번호인증 적용
- 입력불가 단어, 중복체크 유효성 적용
- 중복체크 대상 : 아이디, 닉네임
- 특수문자 제한 대상 : 아이디, 닉네임, 비밀번호
- 형식 제한대상 : 전화번호, 이메일

[로그인]
- 식별가능정보 : 아이디, 비밀번호
- 계정정보가 오류일 경우 틀린 정보내용 응답에 노출 처리

[비밀번호 찾기(재설정)]
- 계정 및 번호인증 후 설정가능
- 아이디와 전화번호로 계정의 유효성을 확인
- 현재 비밀번호와 변경할 비밀번호 비교 및 업데이트

[내 정보 보기 기능]
- 아이디, 전화번호 확인 후 전체 정보 노출