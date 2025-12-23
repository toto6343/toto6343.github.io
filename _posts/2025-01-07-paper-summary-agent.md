---
layout: post
title: "Paper Summary Agent: 논문 요약을 자동화하는 에이전트 만들기"
categories: [AI, NLP, Project]
featured-img: paper.jpg
slug: paper
---

## 프로젝트 소개

**Paper Summary Agent**는  
AI 논문(PDF)을 입력으로 받아 핵심 내용을 자동으로 요약해주는 에이전트입니다.

논문을 읽을 때마다  
- 배경
- 문제 정의
- 방법론
- 실험 결과  

를 빠르게 파악하고 싶다는 필요에서 시작한 프로젝트입니다.

GitHub 레포지토리:  
👉 https://github.com/toto6343/paper-summary-agent

---

## 프로젝트 목표

이 프로젝트의 주요 목표는 다음과 같습니다.

- 논문 PDF에서 텍스트 추출
- 논문의 핵심 구조를 인식
- LLM을 활용한 요약 자동화
- 재사용 가능한 에이전트 구조 설계

---

## 전체 동작 흐름

Paper Summary Agent는 아래와 같은 파이프라인으로 동작합니다.

1. 논문 PDF 업로드
2. 텍스트 추출 및 전처리
3. 섹션 단위 분리 (Introduction, Method, Experiments 등)
4. LLM 기반 요약 생성
5. 최종 요약 결과 출력

---

## 핵심 구현 아이디어

### 1️⃣ 논문 구조 기반 요약

단순히 전체 텍스트를 한 번에 요약하지 않고,  
**논문의 섹션 구조를 기준으로 나누어 요약**하도록 설계했습니다.

이를 통해:
- 정보 손실 감소
- 요약 품질 향상
- 긴 논문도 안정적으로 처리 가능

---

### 2️⃣ 에이전트 패턴 적용

각 단계를 독립적인 역할로 분리하여  
**에이전트 구조**로 구현했습니다.

```python
class PaperSummaryAgent:
    def run(self, paper_text):
        sections = self.split_sections(paper_text)
        summaries = self.summarize(sections)
        return self.merge(summaries)






