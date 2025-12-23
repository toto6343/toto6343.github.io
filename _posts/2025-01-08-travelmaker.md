---
layout: post
title: "TravelMaker: 여행 예약 & 여행 기록 플랫폼 만들기"
featured-img: travel.jpg
slug: travel
categories: [Web, Project, Travel]
---

## TravelMaker 프로젝트 소개

**TravelMaker**는 여행 계획 작성부터  
숙소 예약, 여행 후기 기록, 개인 미니홈피 기능까지 포함된 **올인원 여행 플랫폼**입니다.  
여행을 사랑하는 사용자들이 **여행의 모든 과정을 손쉽게 기록 · 관리**할 수 있도록 설계된 웹 서비스입니다. :contentReference[oaicite:0]{index=0}

GitHub 레포지토리:  
👉 https://github.com/toto6343/travelmaker

---

## 주요 기능 요약

### 🧭 여행 일정 & 다이어리

- 날짜별 여행 기록 입력  
- 일정, 장소, 사진 업로드  
- Kakao Map API를 이용한 위치 검색  
- 여행 기록 캘린더 기능  
- AJAX 기반의 댓글/CRUD 기능 적용 :contentReference[oaicite:1]{index=1}

이 기능을 통해 여행 중 느낀 감정, 장소, 사진 등을  
사용자가 **직관적으로 기록하고 다시 볼 수 있게** 만들었습니다.

---

### 🏠 미니홈피 기능

사용자는 **자신만의 프로필 페이지**를 꾸밀 수 있으며,  
- 프로필 이미지 수정  
- 한 줄 인사말 입력  
- 방문자 수 카운트  
등의 기능을 통해 나만의 여행 공간을 만들 수 있습니다. :contentReference[oaicite:2]{index=2}

---

### 🏨 숙소 검색 & 예약

- 지역, 날짜, 가격, 별점 등 **필터 검색**
- 호텔 썸네일 이미지 및 상세 정보 제공
- 다양한 호텔 데이터 조회 및 예약 UI 구현  
이 기능은 **여행의 핵심인 숙소 선택 과정을 사용자 친화적으로 개선**합니다. :contentReference[oaicite:3]{index=3}

---

### 👥 로그인 & 회원 시스템

- AJAX 기반 아이디/이메일 중복 검사
- 로그인/로그아웃 처리  
- AOP 기반 로그 기록  
사용자 편의성과 보안성을 고려한 회원 시스템을 구현했습니다. :contentReference[oaicite:4]{index=4}

---

## 아키텍처 및 기술 스택

### Backend

- **Java / Spring Boot**
- Spring MVC, MyBatis 기반 REST API  
- Oracle Database  
이 스택을 통해 안정적인 백엔드 구조를 설계했습니다. :contentReference[oaicite:5]{index=5}

### Frontend

- HTML, CSS, JavaScript, jQuery  
- Thymeleaf 템플릿  
- Kakao Map API  
사용자 경험을 고려한 직관적인 프론트엔드 설계가 특징입니다. :contentReference[oaicite:6]{index=6}

### 기타 기술/도구

- Selenium 기반 데이터 수집 (여행지, 호텔 등)  
- Ajax를 통한 비동기 처리 강화  
이로 인해 데이터를 자동으로 수집하고, 실시간 사용자 상호작용을 지원합니다. :contentReference[oaicite:7]{index=7}

---

## 개발 경험 & 배운 점

이번 프로젝트를 통해 다음과 같은 실전 경험을 쌓을 수 있었습니다:

- 복잡한 여행 데이터를 구조화하여 DB에 설계하고 처리  
- 외부 API 연동 (지도, 위치 검색 등)  
- 프론트엔드와 백엔드를 연결하는 REST 구조 설계  
- 사용자 중심 기능(캘린더, 실시간 댓글, 필터 검색) 구현  
이 모든 과정은 **현실 사용자를 위한 기능 설계**에 집중하게 해주었습니다. :contentReference[oaicite:8]{index=8}

---

## 향후 확장 방향

- 모바일 앱 대응 UI/UX 개선  
- AI 기반 여행 추천 기능  
- 사용자 리뷰 기반 랭킹/추천 알고리즘 적용  
- SNS 공유 및 커뮤니티 확장

이런 기능은 향후 사용자 참여율과 플랫폼 가치를 높이는 데 도움이 될 것입니다.

---

## 마무리

TravelMaker는  
**여행의 시작부터 끝까지 기록하고 공유하는 통합 플랫폼**으로서  
실제 여행 경험을 보다 풍부하게 만들어 줄 수 있는 서비스입니다.

이번 프로젝트는 **백엔드 + 프론트엔드 + 외부 API 연동까지 아우르는 전통적인 웹 앱 개발** 경험을 제공했습니다.

앞으로도 더 나은 여행 경험을 위한 기능을 추가해 나갈 예정입니다 🚀
