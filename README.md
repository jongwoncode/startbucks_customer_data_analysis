# Starbucks 고객 데이터 분석을 통한 최적의 프로모션 전략 탐색

# 1. 프로젝트 정보
* 😀 프로젝트 구성원 : 이종원(팀장), 김도환, 성호경, 이현우, 오승훈
* 📆 프로젝트 기간  : 2021.06.01 ~ 2021.06.30
* 🤖 주요 사용 기술  : python, tensorflow, keras, multi-processing


<br>

# 2. 역할

| 팀원 | 담당 역할|
|--|--|
|**이종원[팀장]**|데이터 전처리, 데이터 분석, 데이터 시각화, 보고서 작성|
|김도환|데이터 전처리, 데이터 시각화|
|성호경|데이터 시각화, 가설검정, PPT 제작|
|이현우|데이터 분석, 가설검정, 발표|
|오승훈|데이터 전처리, 데이터 분석, PPT 제작|


<br>

# 3. 분석 결론 : BOGO보다 DISCOUNT가 더 좋은 프로모션 전략이다.

## 3.1 주력 고객층 선정

### 3.1.1 분석 내용

* 50대 ~60대의 고객들이 전체 고객중 44%를 차지하며 가장 많은 비율을 차지하고 있고, 전체 매출의 47.9%를 차지하고 있음.
* 여성이 남성보다 더 큰 금액을 소비하고 있는 모습을 보여줌.

### 3.1.2 주력 고객층 선정
*  **대집단** : 전체 고객중 44%를 차지하며 47.9%의 매출을 올리고 있는 **50대, 60대 고객**을 스타벅스의 주력 고객으로 선정.
*  **소집단** : 전체 고객 중 19.6% 차지하며 24.8%의 매출을 올리고 있는 **50대, 60대 여성**을 주력고객으로 선정.

### 3.1.3 주력 고객층이 선호하는 프로모션
* 주력 고객층은 대집단, 소집단 모두 discount프로모션을 선호하고 그중에 **`fafdcd668e[discount]`**, **`0b1e1539f2[discount]`** 이 프로모션을 공통적으로 선호하는 모습을 보임.
* 총 순수익에 영향력을 강하게 행사하는 주력 고객을 위해서 위 프로모션을 추천.

<br>

## 3.2 총 순 수익 관점에서 우수한 프로모션

* 각 프로모션을 참여(received)된 횟수는 비슷함. 하지만 실제 쿠폰을 사용한 것은 discount가 더 많음. 
* bogo 전략보다, discount 전략이 총 수익 관점에서 좋음.

* reward가 클 수록 completed_ratio가 감소하는 경향을 보임. (상관관계 -0.69)
* **`0b1e1539f2[discount]`** 이 프로모션이 총 수익 관점에서 좋음.
    - 각 프로모션의 참여 빈도가 비슷하며, difficulty가 큼과 동시에 reward 사용 빈도가 적은 것이 total profit에 일조한 것으로 보임.
* 총 수익 관점에서 향후 프로모션을 진행할 때 discount전략을 사용하고, reward를 증가시키더라도 difficulty를 높히는 프로모션을 추천.



## 3.3 신규 고객층이 선호하는 프로모션
* 신규고객은 discount 프로모션을 선호하는 모습을 보여줌. (**`fafdcd668e[discount]`**, **`2298d6c36e[discount]`**)이 두 프로모션을 선호.
* 거래 빈도가 평균보다 높은 신규 고객층을 확보하기 위해서 신규 고객층이 선호하는 위 두가지의 discount 전략을 진행. 
