# 문제설명
* 이번 과제를 통해 여러분은 **음식배달 서비스(배민, 쿠팡이츠 등)를 위한 예측모델** 을 만들게 될 것입니다! 이 모델이 예측하는 값은 **“음식배달에 걸리는 시간"** 입니다. 배달시간을 정확하게 예측하는 것은 사용자의 경험에 많은 영향을 미치게 됩니다.

* 예측된 배달시간보다 **실제 배달시간이 더 걸린 경우(under-prediction)가 반대의 경우(over-prediction)보다 두 배로 사용자의 경험에 안 좋은 영향을 준다** 고 알려져 있습니다.

* 가능한 실제 배달시간과 **가까운 값을 예측하되 동시에 under-prediction을 최소화하는 것** 이 좋은 예측모델입니다.
    
   <br/>

  
# 학습/테스트 데이터
* 파일 “delivery_raw.csv”는 다음과 같은 속성들을 가지고 있습니다.
  * 시간 속성
    * market_id: 지역(배달이 이루어지는 도시) 아이디
    * created_at: 주문이 생성된 시간의 Timestamp(UTC)
    * actual_delivery_time: 주문자가 배달을 받은 시간의 Timestamp(UTC)
  * 식당 속성
    * store_id: 식당 아이디
    * store_primary_category: 식당의 카테고리(italian, asian 등)
    * order_protocol: 주문을 받을 수 있는 방식을 나타내는 아이디
  * 주문 속성
    * total_items: 주문에 포함된 아이템(음식) 개수
    * subtotal: 가격(센트 단위)
    * num_distinct_items: 주문에 포함된 비중복 아이템 개수
    * min_item_price: 주문에 포함된 아이템 중 가장 싼 아이템의 가격
    * max_item_price: 주문에 포함된 아이템 중 가장 비싼 아이템의 가격
  * 지역 상황 속성
    * total_onshift: 주문이 생성되었을 때 가게로부터 10마일 이내에 있는 배달원들의 수
    * total_busy: 위 배달원들 중 주문에 관여하고 있는 사람들의 수
    * total_outstanding_orders: 주문한 가게로부터 10마일 이내에 있는 다른 주문들의 수
  * 다른 모델들의 예측값
    * estimated_order_place_duration: 식당이 주문을 받을 때까지 걸릴 것으로 예상되는 시간(초단위)
    * estimated_store_to_consumer_driving_duration: 식당에서 출발해 주문자에 도착할 때까지 걸릴 것으로 예측되는 시간(초단위)
* 위 속성들 중 actual_delivery_time을 제외한 모든 속성들을 모델의 입력으로 사용할 수 있습니다. 모델이 예측해야하는 값은 actual_delivery_time과 created_at을 사용해서 생성하면 됩니다(초단위로 표현된 두 속성의 차이값).
* 주어진 이 속성들 외에 이것들로부터 파생될 수 있는 속성들을 추가로 만들어서 사용할 수도 있습니다.
    
   <br/>

# 학습/테스트 데이터 구분
* 위 데이터(delivery_raw.csv)에서 랜덤하게 10%를 추출해서 테스트 데이터로 사용하고 나머지는 학습데이터로 사용하세요.
    
   <br/>

# 제출할 결과물
* 간단한 요약문
* 데이터 전처리와 속성 생성에 대한 간단한 설명
* 학습을 위해서 어떤 모델을 사용했는지 그리고 어떠한 손실함수를 사용했는지를 간단히 설명
* 테스트 데이터에 대한 평가지표들 (아래 두가지를 반드시 포함할 것)
  * Root Mean Square Error (RMSE)
  * Under-prediction의 비율 (under-prediction 개수 / 테스트 데이터의 샘플수)
* 모델 학습에 사용한 Jupyter notebook 파일
