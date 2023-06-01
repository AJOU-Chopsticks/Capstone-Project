# Chopsticks
2023-1 아주대학교 소프트웨어 캡스톤디자인 '헤어해죠~' 플랫폼을 제작한 11조 Chopsticks 입니다.

## 팀원
- 201720704 박수길 -조장(back)
- 201820762 목대희 -front
- 201820756 오원석 -front
- 201920772 홍건화 -back
- 201820797 이성규 -back

## 업무 분장
### 개발분야 업무 분장
박수길: database 서버를 관리하거나 세팅하고 각 UI mockup을 검토한다.


목대희: frontend 버전을 확인하고 새 github 프로젝트를 생성한다. 


홍건화: backend 버전을 관리하고 intellij 환경을 구축한다.


오원석: frontend에 관련한 react js를 설치하고 버전을 관리한다.


이성규: backend 버전을 확인하고 각 UI의 연결점을 체크한다.


### 비 개발분야 업무 분장

박수길: 프로젝트 계획을 관리하고 팀원 및 멘토와의 일정을 조율한다.


목대희: PPT발표자료를 관리하고, 예산을 관리한다.


홍건화: 제출물 문서를 관리하고 검토하며 시연 영상을 제작한다.


오원석: 협업 도구를 구성하고 관리한다.


이성규: 기술스택이 맞는지를 검토하고 회의록을 작성한다.


## Pain Point

헤어 스타일에 대한 고민이 많은 고객은 마음에 드는 미용실과 헤어 디자이너를 찾는것이 어렵습니다.


소규모 헤어 디자이너의 경우 최근 헤어 디자이너의 수가 증가함에 따라 경쟁이 심화되어 단골 고객을 유치하기가 어렵습니다.


즉, 고객은 원하는 헤어 디자이너를 탐색하는 것이 필요하고 소규모 헤어 디자이너는 적극적으로 고객을 유치하는 것이 필요합니다.


서울시 1년내 폐업률의 경우 미용실이 11%로 최고라는 기사가 있는 만큼 소규모 헤어 디자이너의 생존은 쉽지 않습니다.


## Solution

저희 헤어해죠~ 서비스는 헤어 스타일 카테고리, 상담기능, 헤어 디자이너 추천 시스템 등을 통해 고객과 헤어 디자이너 모두 만족할 수 있는 양방향 접근 서비스를 제공합니다.


저희 헤어해죠~ 서비스는 크게 1. 일반 매칭, 2. 빠른 매칭, 3. CRMS(고객관계관리서비스)로 구분할 수 있습니다.


1. 일반 매칭의 경우 고객이 먼저 헤어스타일과 관련된 요청 글을 작성하고 헤어 디자이너가 글을 조회하여 상담을 진행합니다. 상담은 실시간 채팅으로 이루어져있으며 텍스트와 이미지 모두 전송 가능합니다. 또한 고객은 헤어 디자이너의 스케쥴에 맞춰서 예약을 진행 할 수 있습니다. 결제는 카카오페이로 진행합니다. 


2. 빠른 매칭의 경우 헤어 디자이너가 업로드한 포트폴리오를 바탕으로 고객이 직접 원하는 헤어 디자이너를 탐색할 수 있고, 지역, 후기, 예약 내역, 관심 헤어 디자이너를 기반으로 한 헤어 디자이너 추천 시스템을 통해 원하는 헤어 디자이너를 찾을 확률을 높일 수 있습니다.


3. 헤어 디자이너의 CRMS는 고객들의 최근 방문 날짜, 방문 횟수를 확인할 수 있으며 특정 고객에 대한 메모를 적고 확인 할 수 있습니다. 또한 월 별, 성별 별, 연령대 별, 메뉴 별, 기존/신규 고객 별 매출을 막대 그래프, 선형 그래프, 원형 그래프로 매출 통계를 확인 할 수 있습니다.   


## System Architecture

![image](https://github.com/AJOU-Chopsticks/Capstone-Project/assets/112956878/ebd67b6b-b37b-4326-aec7-0da2052ea0a8)


-DevOps: github, github action


-Buiness Tools: notion, google drive

|컴포넌트|역할|
|------|-----|
|계정 관리 서비스|회원가입, 로그인, 프로필 조회 및 변경 등 계정 관리 기능을 제공한다.|
|신청 글 관리 서비스|일반 매칭의 신청 글 작성, 수정, 삭제 및 조회 서비스를 제공한다.|
|빠른 매칭 서비스|빠른 매칭의 헤어 스타일 추천 및 원하는 헤어 스타일에 대한 추천 헤어 디자이너 조회 서비스를 제공한다.|
|비대면 상담 서비스|고객과 헤어디자이너 간의 비대면 상담을 위한 실시간 채팅 서비스를 제공한다.|
|후기 서비스|고객의 시술에 대한 후기 작성 서비스와 헤어 디자이너의 후기 조회 및 답글 등록 서비스를 제공한다.|
|CRM 서비스|헤어 디자이너의 고객 관리, 통계 관리, 예약 관리, 재고 관리 등 CRM 기능에 대한 서비스를 제공한다.|
|광고 서비스|광고주의 광고를 신청 및 카카오페이 API를 이용한 광고비 결제 서비스를 제공한다.|
|예약 서비스|고객의 시술 예약 및 카카오페이 API를 이용한 결제 서비스를 제공한다.|
|푸시 알림 서비스|Firebase API를 이용하여 예약, 채팅에 대한 푸시 알림 서비스를 제공한다.|


