---
layout: post
title: "YOLO 프로젝트로 객체 탐지(Object Detection) 이해하기"
featured-img: roadkill.jpg
slug: yolo
categories: [ComputerVision, DeepLearning, Project]
---

## YOLO란 무엇인가?

**YOLO(You Only Look Once)** 는 이미지나 영상에서 객체를 실시간으로 탐지하기 위한  
딥러닝 기반 **Object Detection 알고리즘**입니다.

기존의 객체 탐지 방식과 달리,  
YOLO는 이미지를 한 번만 보고(Bounding Box + Class)를 예측하기 때문에  
**속도가 매우 빠르다는 장점**이 있습니다.

---

## YOLO의 핵심 아이디어

YOLO는 입력 이미지를 **Grid 형태로 분할**한 뒤,  
각 Grid 셀마다 다음 정보를 예측합니다.

- 객체가 존재할 확률
- Bounding Box 좌표 (x, y, w, h)
- 객체 클래스(Class)

이 방식 덕분에 **단일 CNN 네트워크**로  
객체 위치와 분류를 동시에 수행할 수 있습니다.

---

## YOLO 프로젝트에서 구현한 내용

이번 프로젝트에서는 다음과 같은 흐름으로 YOLO 모델을 다뤘습니다.

1. 데이터셋 준비 및 전처리
2. YOLO 모델 구조 이해
3. 학습된 모델을 이용한 객체 탐지
4. 결과 시각화 (Bounding Box 표시)

GitHub 레포지토리:  
👉 https://github.com/toto6343/yolo

---

## YOLO의 장점과 한계

### ✅ 장점
- 매우 빠른 추론 속도 (Real-time 가능)
- 단일 네트워크 구조로 구현이 단순
- 영상 처리에 적합

### ⚠️ 한계
- 작은 객체 탐지에 상대적으로 약함
- 정확도는 2-stage detector(Faster R-CNN 등)보다 낮을 수 있음

---

## 마무리

YOLO 프로젝트를 통해  
**객체 탐지의 전체 파이프라인**을 직접 경험할 수 있었고,  
Computer Vision 분야에서 왜 YOLO가 많이 사용되는지 이해할 수 있었습니다.

추후에는 **YOLOv8**, **커스텀 데이터 학습**,  
그리고 **실시간 스트리밍 적용**까지 확장해볼 계획입니다 🚀








