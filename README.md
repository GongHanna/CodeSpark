# 💻세종사이버대학교 코드스파크(Code Spark) 동아리💻

### 📌 일정 
  - 2025.09.20(토) ~

<br>

### 📌 동아리 목적
  - 포트폴리오를 위해 실전 개발의 경험을 목적으로 하는 동아리

<br>

### 📌 회의
  - 디스코드를 통한 회의

 <br>
 
### 📌 주차별 활동계획
  - 1주차 : 시작 OT, 팀 빌딩, 툴 세팅, 미니 프로젝트 아이디어 선정
  - 2주차 : 미니 프로젝트 기획 - Git/GitHube 실습, 요구사항 분석, 유저 플로우 설계
  - 3주차 : 미니 프로젝트 설계 - ERD, 와이어프레임, IA 설계
  - 4주차 : 미니 프로젝트 개발 1차 - 개발 환경 세팅, 핵심 기능 구현
  - 5주차 : 미니 프로젝트 개발 2차 - 추가 기능 구현, UI 개선, 버그 수정
  - 6주차 : 미니 프로젝트 발표 및 회고

 <br>
 
### 📌 12주 활동 계획
  - 1단계 : 전반 6주 / 미니 프로젝트
      - 미니프로젝트 : 투두리스트, 날씨앱, 가계부 앱, 챗봇앱 등 클론 코딩 가능한 수준의 앱 제작 목표
  - 2단계 : 후번 6주 / 메인 프로젝트
      - 신규 아이디어를 통한 기획 ~ 개발 ~ 유지보수 가능한 앱 개발 목표
    

 -----------------------------------


## 💡 선정된 미니 프로젝트

<br>

 * 미니 프로젝트 1 - 투두리스트
   - [x] 리드 팀원 : 심효진님
   - [x] 참여 팀원 : 공한나님, 김주영님, 심효진님
   - [x] 사용 툴 : 디자인 - Figma, 프론트 - React, 백엔드 - Node.js
   - [x] 역할 분담 : 디자인/프론트 : 김주영님, 공한나님, 백엔드 : 심효진님, QA/문서화 : 모든 팀원
  
  <br>

  * 미니 프로젝트 2 - 날씨앱
    - [ ] 리드 팀원 : 미정
    - [ ] 참여 팀원 : 심효진님
    - [ ] 사용 툴 : 미정

  
 -----------------------------------

  

## ✏️ 미니프로젝트 진행상황

👉 [SCHEDY 보러가기](https://gonghanna.github.io/CodeSpark/)

### 2025.11.04
* 반응형 css 수정

### 2025.11.02
* 드래그앤드롭 기능 추가 완료 [참고자료](https://github.com/hello-pangea/dnd)
  * 리액트에서 드래그 앤 드롭(Drag and Drop) 기능을 쉽게 구현할 수 있게 도와주는 라이브러리 사용 => @hello-pangea/dnd
  * 기본 구조는 세 가지 컴포넌트/훅으로 이루어져 있음 :
```
<DragDropContext onDragEnd={handleDragEnd}>
  <Droppable droppableId="droppable-id">
    {(provided) => (
      <div ref={provided.innerRef} {...provided.droppableProps}>
        {items.map((item, index) => (
          <Draggable key={item.id} draggableId={item.id} index={index}>
            {(provided) => (
              <div
                ref={provided.innerRef}
                {...provided.draggableProps}
                {...provided.dragHandleProps}
              >
                {item.content}
              </div>
            )}
          </Draggable>
        ))}
        {provided.placeholder}
      </div>
    )}
  </Droppable>
</DragDropContext>
```
  * DragDropContext → 드래그 이벤트 관리
  * Droppable → 드롭 가능한 영역
  * Draggable → 드래그 가능한 요소
  * 순서 변경 & 상태 관리 :
    * 드래그 후 손을 떼면 onDragEnd 이벤트가 호출됨
    * 이벤트 핸들러에서 source.index와 destination.index를 사용하여 배열 순서를 재정렬하고 상태(state)를 업데이트

### 2025.11.01
* 스크롤바 이슈 수정 완료
* 기존에 있던 구조 수정
  * ul>li 구조에서, div>ul>li 구조로 수정 후, ul에 적용하던 padding을 div에 적용 및 그 외 css 수정
  * 스크롤 감지할 스크립트 코드 추가 작성

### 2025.10.26
* 각 기능별로 컴포넌트 및 페이지 분류 후, 헤더, 홈화면, 투두리스트 제작

### 2025.10.21
* Figma를 이용해 로고제작, 로그인창 및 회원가입창 제작(디자인 및 워크플로우 완성)
* [Schedy 디자인](https://www.figma.com/design/gifSGacObr90fE6KBeQrcm/SCHEDY_TODO-%EB%94%94%EC%9E%90%EC%9D%B8%EC%A0%9C%EC%9E%91?node-id=43-747&t=LdKwD2EZojdXhAaS-0)

### 2025.10.20
* Figma를 이용해 투두 기능, 로그인 창, 스타일 시트 작성

### 2025.10.18
* [주간 회의 보고서](https://github.com/Code-spark-dev/todo_list/wiki/10.18-%EC%A3%BC%EA%B0%84%ED%9A%8C%EC%9D%98)
* Figma를 이용해 기능 정리 및 화면 구성

  
 -----------------------------------

  

## ✏️ 개인 공부


### 2025.10.26
**Schedy 리액트 디자인**
* [x] 홈화면 제작
* [x] 헤더와 투두아이템 컴포넌트 제작
* [ ] 이슈 발생 : 스크롤의 위치를 변경할 수 없음 -> 추후에 기존 스크롤바를 대체할 코드 넣어야 함 

### 2025.10.02 ~ 2025.10.04
**개발하고 싶은 프로젝트와 협업 도구에 대한 스터디**
* [x] 깃허브 복습 및 코드 스파이크 회의 내용 정리
* [x] 투두리스트 앱 개발 스터디
  * 필수 기능 :
    - 회원가입 / 로그인 (이메일, 구글 로그인)
    - 할 일 추가 : 새로운 할 일 항목을 입력하고 리스트에 추가하는 기능
    - 할 일 수정 : 기존에 등록된 할 일의 내용을 변경하는 기능
    - 할 일 삭제 : 리스트에 있는 할 일을 제거하는 기능
    - 할 일 완료 : 할 일을 완료 상태로 표시하고 시각적으로 구분하는 기능
    - 마감일 설정 : 각 할 일 항목에 마감일을 부여하여 중요도와 긴급성을 파악하고 일정을 관리하는 기능
  * 부가 기능 :
    - 카테고리/태그 기능 (예: 공부, 운동, 업무)
    - 알림 기능 (오늘 할 일 푸시 알림)
    - 드래그 앤 드롭으로 순서 변경
  * 사용 언어 : 프론트엔드(React or Vue.js) + 백엔드(Node.js or Python)
  * 역할 분배 :
    - 기획 & 디자인 담당 → 와이어프레임 / UX 설계
    - 프론트엔드 담당 → 화면 개발
    - 백엔드 담당 → API 서버, DB 연결
    - QA & 문서화 담당 → 기능 테스트, 배포, 사용 매뉴얼 작성

<br>

**1. 선택한 언어/스택에서 실습 가능한 기능 & 기술**
* 프론트엔드 (React or Vue.js) : 
  - 상태 관리 → 할 일 목록 상태 추가/수정/삭제 (ex. React의 useState, useReducer, Vue의 reactive, Vuex)
  - 컴포넌트 설계 → 할 일 항목, 리스트, 입력 폼 등을 모듈화
  - 폼 처리 & 유효성 검사 → 로그인, 회원가입 입력값 확인
  - API 연동 → 백엔드에서 제공하는 REST API 호출 (axios, fetch)
  - UI/UX 개선 → 마감일 시각적 강조, 완료 항목 스타일링, 드래그 앤 드롭 구현
* 백엔드 (Node.js / Python) :
  - REST API 설계 → CRUD(Create, Read, Update, Delete) 구현
  - 인증 & 보안 → JWT 토큰 인증 / OAuth(구글 로그인)
  - DB 연동 → MongoDB, MySQL, PostgreSQL 등 사용 (스키마 설계 & 데이터 CRUD)
  - 에러 처리 & 로깅 → 안정적인 서버 구축 경험
  - 알림 기능 → 푸시 알림 (Firebase Cloud Messaging)
* 공통 :
  - 배포 경험 → Vercel(프론트엔드) + Render/Heroku(백엔드) or AWS 사용
  - 협업 툴 사용 → Git/GitHub로 브랜치 전략, PR 리뷰, 이슈 관리
  - API 문서화 → Swagger, Postman으로 API 테스트 및 문서 작성

<br>

**2. 선택한 언어의 효율성**
* 프론트엔드: React 추천 : 
  - 자료가 많고, 기업에서도 실무에서 가장 많이 사용
  - 컴포넌트 기반 설계에 익숙해지면 다른 프레임워크(Vue, Angular)로 확장 쉬움
* 백엔드: Node.js 추천 :
  - 프론트/백 모두 JavaScript 하나로 통일 가능 → 학습 효율 ↑
  - 실무에서도 스타트업/프로덕트 초기 개발에 많이 쓰임

<br>

**3. 프로젝트를 통해 키울 수 있는 역량**
* 기술적 역량 :
  - 풀스택 개발 경험: 프론트(React) + 백엔드(Node) + DB까지 전 과정 경험
  - 실전 협업 경험: Git을 활용한 브랜치 전략, 코드 리뷰, 역할 분배
  - 배포 역량: 실제 웹에서 돌아가는 서비스 배포 경험
  - API 설계 & 연동 능력: RESTful API에 대한 이해
* 비기술적 역량 :
  - 문제 해결 능력: 버그 해결, 에러 로그 분석, 대안 찾기
  - UX 관점: 단순히 기능이 아닌 “사용자가 편리하게 쓸 수 있는 UI/UX” 고민
  - 팀 커뮤니케이션: 역할 분담, 일정 조율, 협업 경험
  - 문서화 & 발표 능력: 기능 정의서, API 명세서, 사용 매뉴얼 작성
