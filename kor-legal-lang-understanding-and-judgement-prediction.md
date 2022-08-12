# A Multi-Task Benchmark for Korean Legal Language Understanding and Judgement Prediction
![image](https://user-images.githubusercontent.com/39285147/184294516-0dad2074-9c87-44f1-af52-6ea4c0b5f174.png)

[**논문**](https://arxiv.org/abs/2206.05224)

# 들어가기 전

법률 계약서는 일반인은 독해하기 어려운 단어들 뿐만 아니라, 한 문장이 한 페이지를 차지할 정도로 긴 문장들을 포함한다.

이전에 참가한 한 세미나에서는 이러한 법률 계약서에 존재하는 오류를 검사하는 AI 모델을 실제 변호사와 대결시킨 사례를 소개했다.

AI 모델은 **26초 만에 94%의 정확도**로 오류를 검증해내었고, 반면 사람 변호사는 **96분 동안 86%의 정확도**로 오류를 잡아냈다.

매번 적응되지 않을 정도로 AI의 능력은 정말이지 어마무시하다.

하지만, 상기 법률 계약서는 영어로 적힌 문장들로 구성이 되었다. 다시 말해, 자연어 처리 분야에서 기계독해가 까다로운 **한국어로 적힌 법률 계약서**는 아직까진 그만한 성능을 내는 AI 모델이 전무할 것이다.

상기 목표를 달성하기 위해서는 다양한 조건이 수반되어야 할터인데, 가령 한국어 기반 모델 검증을 위한 **법률 평가 데이터셋**이 필요할 것이고, 까다로운 한국어 문법을 정확히 이해하여야 할 것이다.

여기까지는 내 잡담이었으니 가볍게 무시해도 상관없다.

하지만, 앞서 언급된 사례는 다양한 전문 분야에서 **한국어 기반 NLP 연구**의 필요성을 부각한다.

# ABSTRACT
최근 발달한 딥러닝 기술로 인해 자연어 처리 분야 역시 많은 변화가 있었고, 이러한 변화의 물결은 법률 분야에 이르렀다.

하지만, 해당 전문 분야에 대한 **한국어 NLP 데이터셋 부재**와 NLP 학습에 **까다로운 한국어 특성**이 발목을 잡았다.

그래서, 서교수를 주축으로한 연구팀은 '최초로' **한국어 기반 대용량 법률 AI 데이터셋**과 **'LBOX OPEN'**이라는 법률 평가 데이터셋, 그리고 **LCUBE라는 한국어 법률 언어 모델**을 만들게 되었다 (*LBOX OPEN과 LCUBE는 해당 논문 페이지를 통해 다운받아 이용 가능하다*).

LBOX OPEN은 *1개의 법률 corpus*, *두 개의 분류 문제*, *두 개의 법률 판단 예측 문제*, 그리고 *한 개의 요약 문제*를 위한 평가 데이터셋이다.

> 범죄와 같이 어떠한 종류의 사례들을 기반으로 구성된 데이터셋인지, 언제/어떻게 데이터를 수집했는지와 같은 보다 자세한 내용은 해당 논문에서 확인하길 바란다.

# INTRODUCTION
이전에 규칙과 도메인 지식에 근거한 법률 시스템은 유의미한 성과를 내기도 했으나, 범용성이 부족하다는 한계점이 존재했다.

하지만, Deep Learning에 발전에 따라 자연어 처리 또한 많은 변화의 시기를 거쳐서 '판결 예측'과 같은 여러 법률 분야에 새로운 기술적 패러다임을 제시한다.

이러한 격동의 시기에 발맞춰 전세계에서는 AI 모델 학습에 필수적인 법률 데이터셋을 만들기 시작했고, 서교수님 연구실 또한 기존에 정부에서 내놓은 활용 가치가 떨어졌던 한국어 법률 데이터셋에서 확장하여 새로운 한국어 기반 법률 데이터셋 연구 개발에 임하게 되었다.

# LBOX OPEN - Large-scale Korean legal AI benchmark.

(1) **a large-scale legal precedent corpus** (PRECEDENT CORPUS)

(2) **two classification tasks** (CASE NAME, STATUTE)

(3) **two legal judgement prediction tasks** (LJP-CRIMINAL, LJPCIVIL)

(4) **one summarization task** (SUMMARIZATION).

# LCUBE - Language model based on LBOX OPEN
**Classification tasks**
- GPT-2 활용 decoder-only 모델 --> comparable performance with MT5 (a competitive encoder-decoder language model with larger size)

**Summarization tasks**
- 타모델에 비해 상대적으로 안좋은 성능을 보인다.




