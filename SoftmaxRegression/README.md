# 규제화를 사용한 모델학습
* Softmax Regression.ipynb에 있는 코드를 수정해서 다음을 구현해보세요.
  * L2 regularization을 비용함수(compute_cost 내에)에 포함시키고 gradient 계산에(batch_gd 내에) 반영하세요.
  * Regularization을 위한 가중치 lambda를 튜닝해보세요.
    * 이것을 위해서 학습데이터의 일부를 validation data로 따로 구분하고 이 validation data에 대한 accuracy를 최적화하는 lambda를 찾도록 하는 코드를 구현해보세요.

# 다중클래스 분류모델의 결정경계 구하기
* 아래 웹페이지에서 두 가지의 모델이 학습됩니다. 그 중에서 'multinomial' logistic regression의 경우에, 결정경계를 나타내는 방정식들을 구하고 화면에 나타내보세요.
  * https://scikit-learn.org/stable/auto_examples/linear_model/plot_logistic_multinomial.html
* 아래 이미지처럼 결정경계는 세 개의 직선방정식으로 나타낼 수 있습니다. 즉, 클래스1과 클래스2의 경계를 나타내는 직선방정식, 클래스1과 클래스3의 경계를 나타내는 직선방정식 그리고 클래스2와 클래스3의 경계를 나타내는 직선방정식입니다. 방정식들을 구하고 화면에 그려보세요.
  <img src="https://scikit-learn.org/stable/_images/sphx_glr_plot_logistic_multinomial_001.png" width="700px" height="500px" alt="RubberDuck"></img><br/>
