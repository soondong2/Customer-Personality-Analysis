# Customer Personality Analysis Project
![dataset-cover](https://user-images.githubusercontent.com/100760303/198925583-26b5e6e9-7373-4b39-bf52-925e30bb8ab5.png)

<br>

## 상세 내용
![캡처](https://user-images.githubusercontent.com/100760303/198926107-9f9a3290-122f-4e81-bfcb-d5187c3b8e57.PNG)

소비자 데이터를 통해 기업의 입장에서 고객 데이터를 분석합니다.
분석한 내용은 다음과 같습니다.

1. 소비자 유형 분석
    1. 주 고객층의 연령대
    2. 연령대에 따른 상품 카테고리별 결제 금액
<br>

2. 물품 구입 경로 및 구매 성향 분석
    1. 선호하는 구매 경로
    2. 자녀의 수에 따른 구매 경로
<br>

3. 캠페인 성과 분석
    1. 캠패인 이용자의 소비 패턴과 특성을 분석하여 장기적인 투자 여부 결정
    2. 지난 캠페인 성과를 포함한 캠페인 차수 간에 상호연관성 분석
    3. 캠페인을 통해 유입되는 주 소비자 유형 분석
<br>

4. RFM 분석으로 각 고객군별 매출액을 확인 후 프로모션 전략 제시

<br>

## 파생변수
- `Age` : `Year_Birth` 고객의 생년월일 컬럼을 이용해 `Age` 나이 컬럼 생성 후 생년월일 컬럼은 삭제하였습니다.
- `Age_range` : 연속형 변수인 나이를 분석하고 시각화하는데 활용하기 위해 구간화하여 청년, 장년, 중년, 노년으로 구분하는 파생변수를 생성합니다.
- `Children` : Kidhome은 총 자녀의 수, Teenhome은 자녀 중 청소년인 자녀의 수로 이해를 했으나 데이터를 살펴보니 의문점이 생겼습니다. Kidhome은 0명인데 Teenhome은 1명 이상인 값들이 보이고 있습니다. Teenhome은 청소년인 자녀를 나타내고, Kidhome은 총 자녀의 수 - 청소년 자녀의 수를 나타내는 게 아닐까? 라는 생각이 들어, 총 자녀의 수를 나타내는 Kidhome + Teenhome = `Children` 라는 변수를 생성합니다.
- `Total_Accepted` : 캠페인 컬럼을 살펴보니 이전 캠페인을 수락했더라도 다음 캠페인을 또 다시 제안 받을 수 있고, 수락이 가능한 것으로 판단되어 총 캠페인 수락 횟수를 나타내는 `Total_Accepted` 변수를 생성합니다.
- `Total_spent` : 와인, 과일, 고기, 어류, 사탕, 금에 사용한 총 금액을 나타내는 `Total_spent`  파생변수를 생성합니다.
- `Expenditure_ratio` : 소득 대비 소비자가 소비에 사용하는 금액 비율을 산출하여 파생변수를 생성합니다.

<br>

## 분석 결과
https://www.notion.so/soondong/Customer-Personality-Analysis-7fec08e6489649869b85174615bcb264
