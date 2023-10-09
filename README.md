
![header](https://capsule-render.vercel.app/api?type=waving&color=auto&height=300&section=header&text=빅데이터콘&fontSize=90)

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white"> <img src="https://img.shields.io/badge/jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white">

### 데이터 출저
예술의 전당 데이터를 사용

-------------------------------


### 목적
클래식 공연 활성화를 위한 예술의전당 콘서트홀의 효과적 가격 모델 수립

------
### 분석 배경 및 목적
동적 가격 제도(dynamic pricing): 특정 기준에 따라 가격을 달리 함으로써 매출을 늘리기 위한 전략.

- 서비스 산업에서도 동적가격이 보편적인 전략으로 변화되고 있음을 감안한다면 공연예술산업에서도 동적가격전략의 적극적인 도입이 필요한 시점

- 일반적으로 공연예술의 분야는 공공재의 인식이 있기 때문에 다른 산업군에 비해서 비교적으로 상품의 범용화 단계에 있다고 보기도 어렵고, 탄력성에 관한 상황도 동적가격 도입을 위한 조건을 충족하지 않는 경우가 있음. (가격이 비탄력적임)

- 그러나, 예술업계에서 기부금과 멤버십으로 사용하는 시스템으로 이러한 기부금으로 비영리 공연예술조직을 설립하여 신규 단골 고객을 포섭하는 방식을 사용
실제로, 한 연구결과에 따르면, 공연예술 구매자들의 가격 공정성 지각이  동적 가격제의 도입에 따라 유의미한 결과가 있는지를 연구하자, 부정적인 의견이 적을 것이라는 결과

---------------------------
### 분석 과정

1. 데이터 군집화
   - 동적 가격제 적용을 위한 예매율이 낮은 공연을 군집화

2. 예매율 특징 분석
   - 예매율이 낮은 군의 특징의 특징을 분석
   - 할인율의 적용의 가능성을 분석
3. 예매 예측 및 동적 가격 적용 비교
   - 군집화에서 선출된 군의 값들의 예매취소여부를 예측
   - 구간별로 나눈 값에 할인율 적용 및 예매취소 재 예측
   - 동적가격제의 효과 비교
-------------------------------------
### 전처리 (Preprocessing) 항목
'상당한 결측치들의 존재를 보고 데이터 여부 선정의 우선순위를 정하는 것을 목표로 정함'
- Membershiptype = >  타입1~6에 입력되는 기준을 등급순으로 순차적 배정
- SEAT = > 공연마다 좌석 기준이 다르고 좌석도 여러개여서 하나씩 확인하여 장소별로 분류하고 기준을 정함
- grade => R / S / A / B / C / 전체 일반석   분류
- tokenized_discount: 할인 유형에 따라 8가지의 할인 유형을 만들어 토큰화 변환
- discount_type_count: 공연당 사용된 할인 유형의 갯수
- Time_category: 기준에 따라 오전/오후/저녁으로 분류
- date_difference: 공연날짜 - 공연예매일
- day_of_week: 요일 토큰화
- is_holiday: 공휴일 유무
- reservation_rate: 예매율
- corona_reg: 공연당일 단계별 코로나 규제 단계
- corona_infected: 서울시 당일 코로나 추가 확진자


   
![footer](https://capsule-render.vercel.app/api?section=footer&height=100)
