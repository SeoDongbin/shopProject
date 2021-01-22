# ShopProject 프로젝트 설명서

- 프로젝트명 : Y-Market(웹 쇼핑몰)
- 시 행 처 : 연성대학교
- 수 행 기 간 : 2020.04.03 ~ 2020.06.25 (약 80일 소요)
- 주 요 역 할 : PM(Project Manager)
- 구 성 원 : PM 외 2명
- 개 발 환 경 : TomCat 8.5 / Oracle 11g / JDK 14 / Spring Framework 3.9.4 / Eclipse 4.15.0

- 기 능 구 현 : 회원 관리 (회원가입, 로그인, 비밀번호 찾기, 개인정보수정, 회원탈퇴)
               상품 관리 (카테고리, 검색, 구매, 즐겨찾기, 장바구니, 배송확인)
               후기 관리 (후기 남기기, 후기 수정, 후기 삭제)

- 산 출 물 : 분석 단계 (프로젝트 계획서, 요구사항 정의서 및 추적표, 프로세스 정의서, ERD(Entity Relationship Diagram), CURD Matrix)
             설계 단계 (논리적 모델링, 물리적 모델링, 메뉴구조도, 화면설계서, 테스트계획서)
             구현 단계 (주간보고서, 테스트 보고서, 소스 코드, 프로젝트 완료 보고서)

- 기 능 설 명
 ○ 회원관리
  - 회원가입 : 주소 API를 이용한 주소검색 시스템 이용
  - 로그인 : AJAX를 이용해 ID 혹은 PW 불일치 시 메시지 출력 로그인 성공시 session을 이용해 로그인 유지
  - 비밀번호 찾기 : ID 와 E-mail 정보를 받아 AJAX를 이용해 일치 판별 후 일치 시 난수 6자리로 비밀번호 변경 후 변경안내 메시지 출력
  - 개인정보수정 : ID, 성별, 주민등록번호는 변경 불가항목
  - 회원탈퇴 : 주의사항 안내와 함께 PW와 주민등록번호를 기입 후 탈퇴 완료(단, 선분이력관리를 위해 DB에선 실제로 삭제되지 않고 end_date 날짜가 9999-12-31일로 update됨)
  
  ○ 상품관리
   - 카테고리 : 사이드 바를 이용해 선택한 카테고리에 맞는 상품을 구성
   - 검색 : 상품이름의 일부분과 일치하는 상품을 구성
   - 구매 : 선택된 상품들의 정보와 총 구매합계액을 출력, 배송지변경과 결제수단 선택가능 구매완료시, 구매를 가정한 완료페이지로 이동
   - 장바구니 : 장바구니 페이지에서 등록한 상품 삭제가능, 상품상세 페이지에서 추가 삭제 AJAX를 이용해 구현(장바구니 상태에따라 버튼이름 변경)
   - 배송확인 : 결제가 완료된 상품들의 배송상태를 확인가능
   
  ○ 후기관리
   - 후기남기기 : 배송완료된 상품에 한정하여 1개의 후기만 등록가능
   - 후기수정 : 등록한 후기를 수정
   - 후기삭제 : 등록한 후기를 삭제
   
 -그 외 사용기술
   Maven / MyBatis / JSTL / 커맨드객체 / JQuery
 
- 보완 사항
 Spring Security를 이용한 로그인 체계 강화
 Transaction 관리
 AOP 디자인패턴 적용
 결제모듈이용
 Restfull API 구현
 Exception 처리
   
