# 머신러닝 회귀 기반 농업인 손상자 수 추정을 위한 빅데이터 분석
[제 1회 빅데이터 분석 경진대회 1위 수상작] [22 대한의용생체공학회 추계 학술대회 논문 게재]

2021.11 ~ 2021.12 (2개월) [경진대회 보고서.pdf](https://github.com/DOYOON510/Farmers-injured-analysis/files/11480799/default.pdf)

## 📗 목차
  - 👨🏻‍💻 담당업무
  - ✍️ 서론
  - 📑 프로젝트 내용
    - 데이터 전처리
    - 모델링
    - 농업인의 손상요인 분석
  - 🏆 결과 및 성과
  - 💡 Insight

## 👨🏻‍💻 담당업무
- 팀장 - 팀 프로젝트 진행 관리, 구성 기획 및 업무 분담, 발표
- 분석방법론 설계 및 검증
- EDA
- 데이터 전처리
- 모델링

## ✍️ 서론
- 농촌진흥청 국립농업과학원에 따르면 2019년도까지 농업인의 손상율은 약 2.6%, 한국의 농업 분야 업무상 사고 재해율은 9.7%로 재해 위험률이 높은것을 확인할 수 있다.
- 이처럼 농업분야 사고율이 높기 때문에 어떠한 요인이 손상에 많은 영향을 미치는지 분석할 필요가 있다.
- 본 연구는 **농업인의 업무상 손장자수를 예측하고, 이를 통해 농업사고 원인을 분석하며 향후 농업인의 업무상 손상요인 제거와 예방**을 목적으로 한다.

## 📑 프로젝트 내용
### 1. 데이터 전처리

- 데이터 문항들의 측정 점수 단위가 일정하지 않아 등간척도 및 리커트 척도를 이용하여 데이터 변환
- 성별 및 예/아니오 와 같은 문항은 binary로 데이터 변환하며, 손상 여부는 target 변수로 설정
![image](https://github.com/DOYOON510/Farmers-injured-analysis/assets/129147977/5acf6401-fb9a-4d1a-88e6-b23235993f83)

- 총 조사인원이 13327명, 손상자는 382명 이었으며, 테스트 데이터의 총 인원은 4443명, 손상자는 122명으로 설정

### 2. 모델링

- 시군구명을 기준으로 변수 값을 통합한 뒤, 6가지 머신러닝 모델(Gradient boosting, Random forest , NGB  등)을 사용하여 교차검증 진행하며 지역별 손상자 수 를 예측
![image](https://github.com/DOYOON510/Farmers-injured-analysis/assets/129147977/d44f38e7-3cf5-430f-98ca-f84da71e531a)

- RMSE를 평가지표로 사용하여 학습결과를 분석해본 결과, NGB regressor모델이 약 0.08로 RMSE 값이 가장 적은것을 확인하며 지역별 손상자 수를 예측하기 위한 최종모델로 선정
![image](https://github.com/DOYOON510/Farmers-injured-analysis/assets/129147977/f69bf4b3-b1d2-4264-ad24-95c58c32e3ac)

- 농업인의 손상여부를 확인하기 위해 target을 0,1로 설정하여 6가지의 머신러닝 회귀모델(Gradient boosting, Random forest, XGB 등)을 사용하여 모델학습
- 정확도를 평가지표로 설정하여 정확도가 가장 높은 Random forest 모델을 손상여부를 판단하는 최종모델로 선정하여 특성중요도 추출

### 3. 농업인의 손상요인 분석

- Random forest 모델을 사용하여 특성중요도를 추출하여 상위 10개의 주요 손상요인을 확인 및 분석
- 손상자수를 추정하는 머신러닝 학습결과의 상위 데이터와 특성중요도의 상위 3개 문항을 사용하여 추정결과를 분석



## 🏆 결과 및 성과
- ‘제 1회 데이터 분석 경진대회’에서 1위 수상
- 22 대한의용생체공학회 추계 학술대회 논문 게재
    - 22 대한의용생체공학회 추계 학술대회 발표논문집 p.455-456
- 농업인의 지역별 손상자 수를 추정할 수 있는 예측 모델 개발
- 농업인의 주요 손상원인을 확인 및 분석

## 💡 Insight
- 모델링을 진행하며 변수 선택 및 모델 선택의 중요성을 알게됨
- 특성중요도가 계산되는 전반적인 과정을 알 수 있었으며, 특성중요도의 활용하여 프로젝트를 진행할 수 있는 역량을 기를 수 있었음
