# 실전 프로젝트 - CNN을 활용한 풍경(Scene) 이미지 분류
* 한 장의 풍경 이미지가 주어졌을 때, 어떠한 카테고리(category)에 속하는지 맞히는 분류 모델을 만드세요.
* 다음의 세 가지 대표적인 CNN 모델을 실습합니다.
  * [LeNet (1998)](http://vision.stanford.edu/cs598_spring07/papers/Lecun98.pdf)
    
  <img src="https://blog.kakaocdn.net/dn/bChW5M/btqTKLpO6ST/bfZ99UcRuKz1xC7LwgrtB0/img.png" width="600px" height="250px" ></img><br/><br/><br/>

  * [AlexNet (2012 NIPS)](https://proceedings.neurips.cc/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf)
    
   <img src="https://neurohive.io/wp-content/uploads/2018/10/AlexNet-1.png" width="600px" height="300px" ></img><br/><br/>
   
  * [ResNet (2016 CVPR)](https://arxiv.org/abs/1512.03385)

  <img src="https://wikidocs.net/images/page/137252/12.png" width="400px" height="300px" ></img><br/><br/>
    
* 성능을 올릴 수 있는 두 가지 심화 기법을 실습합니다.
  * [Mixup (ICLR 2018)](https://arxiv.org/abs/1710.09412): 데이터 증진 기법의 일종으로 정확도를 높입니다.
  * Transfer Learning: 학습 속도와 정확도를 모두 향상시킬 수 있습니다.
  
</br>
   
* 본 프로젝트는 총 **7개의 문제** 로 구성됩니다.
  * **Problem** 이라고 명시된 부분의 소스코드만 작성합니다.
  * **알아보기** 라고 명시된 부분은 단순히 읽고 실행하면 됩니다.
  * 단계적으로 문제를 풀어나가는 과정에서 CNN 기반의 고성능 분류 모델을 학습하는 방법을 이해할 수 있습니다.
* (참고) 본 실습 코드에서는 빠른 결과 도출을 위해 30~50 epoch 정도만 학습합니다.
  * 풍경 데이터셋에 대하여 완전히 학습시키기 위해서는 100 epoch 이상의 학습이 필요합니다.
