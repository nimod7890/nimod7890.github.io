---
title: Autogressive Model
layout: post
categories:
  - Generative Model
permalink: /categories/Generative Model
---

# Autogressive model

이미 생성된 자신의 데이터를 이용해서 나머지 데이터를 생성하는 모델

생성할 데이터가 n차원이라고 가정,

### $$p(x)=p(x_1,\dots,x_n)=\Pi_{i=1}^n\ p(x_i|x_1,\dots,x_{i-1})$$

모든 차원의 결합 확률분포(이전 차원에 대한 조건부확률분포를 순차적으로 구함)

= 각 차원의 조건부 확률분포의 곱

→ 모든 $$x_i$$가 관측변수가 되기 때문에 FVBN(Fully Visible Belief Network)라고 부름

장점: 모델이 단순해서 안정적인 학습 가능

단점: 순차적으로 하나의 차원씩 생성해야 하기때문에 속도가 매우 느림
