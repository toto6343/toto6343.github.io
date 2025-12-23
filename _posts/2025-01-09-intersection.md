---
layout: post
title: "교차로 돌발진입 감지 시스템: Intersection 프로젝트 소개"
featured-img: intersection
slug: intersection
categories: [AI, ComputerVision, Project]
mathjax: true
---

## 프로젝트 개요

**Intersection**은 교차로에서 발생할 수 있는 차량의 **돌발진입 상황**을 자동으로 감지하는  
비전 기반 감지 시스템 프로젝트입니다.  
이 시스템은 실시간 영상 데이터를 활용해 위험 상황을 포착하고,  
추후 **안전 알림/경고 시스템**으로 확장할 수 있는 기술적 기반을 제공합니다.

👉 GitHub 레포지토리:  
https://github.com/toto6343/intersection

---

## 프로젝트 배경

교차로는 교통 사고와 돌발 상황이 자주 발생하는 공간입니다.  
따라서 **실시간 위험 감지** 기술은 교통 안전 시스템에 매우 중요합니다.

Intersection 프로젝트는 다음과 같은 문제를 해결하고자 했습니다:

- 일반 카메라 영상 기반 위험 상황 자동 탐지
- YOLO 기반 객체 탐지 모델 적용
- 실시간 판단/경고 시스템 구현

프로젝트 수행 과정에서는 데이터 수집, 전처리, 모델 학습, 분석까지  
**전체 파이프라인**을 직접 경험했습니다.

---

## 전체 파이프라인

Intersection 시스템은 다음과 같은 단계로 동작합니다:

### 1️⃣ 데이터 수집 & 자동 라벨링
- 영상 데이터 수집
- 자동 라벨링 과정으로 객체 주석 생성

### 2️⃣ 데이터 전처리
- Train / Valid / Test 분리 (8:1:1)
- 이미지 리사이징 및 정규화

### 3️⃣ 모델 학습 및 튜닝
- YOLO 모델 사용
- 신뢰도(Confidence) 기반 예측 성능 평가

### 4️⃣ 실시간 검출 및 시각화
- 실시간 영상 입력 시 검출 결과 표시
- 대시보드 연동으로 결과 확인 가능

---

## 핵심 구성 요소

### 📌 객체 탐지 모델

프로젝트에서는 **YOLO 아키텍처 기반 모델**을 사용했고,  
실시간 처리 속도와 정확도의 균형을 고려해 모델 구조를 선택했습니다.

```python
# 모델 실행 예시
results = model.predict(frame)

for box in results.xyxy[0]:
    # detection logic
    pass
