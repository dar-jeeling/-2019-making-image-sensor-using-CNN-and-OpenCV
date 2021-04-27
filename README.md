# coating-classification-withCNN
predicting semiconductor coating statement with CNN
2019년에 진행했던 CNN을 이용하여 반도체 박막의 코팅 상태를 non-conformal과 conforaml로 판단하는 프로젝트입니다.
2년 전에 진행했던 프로젝트이기 때문에, 코드 중 일부가 현재 시점에서 유실되었습니다.

(프로젝트 동기)

 반도체 박막의 증착 과정 중 모양이 conformal한 경우에는 정상 작동하지만, non-conformal 한 경우에는 정상적으로 작동하지 않을 가능성이 높음.
 보통 초음파 센서를 사용하여 이를 판별해내지만, 초음파 센서의 경우 외부의 개입으로 인하여 결과가 불확실해질 가능성이 있기 때문에
 CNN을 이용한 이미지 센서를 제작하고자 함.
 ![conuncon](https://user-images.githubusercontent.com/74234333/116227259-e8ed6a00-a78e-11eb-886a-653b28f473b0.JPG)

(a) conformal (b) non-conformal
(이미지 출처 : https://www.researchgate.net/figure/a-Conformal-deposition-b-Nonconformal-deposition_fig7_35492417)

(원리 및 방법)

 CNN을 이용하여 conformal한 이미지와 non-conformal한 이미지를 구분하여 binary로 학습을 시킴.
 위의 이미지를 대량으로 구하기 어려웠기 때문에 ImageGenerator를 사용하였음.
 
(어려웠던 점)

 - 이미지 데이터를 구하기 어려워서 ImageGenerator를 사용하였으나, 이미지의 갯수가 극소수(6개...)였기 때문에
 정확한 센서를 만들기 어려웠음.
 - 적은 데이터로 학습을 시켰기때문에 비정상적인 정확도가 만들어짐
 - 따라서, 차선책으로 unconformal한 cell의 모양과 conformal한 cell의 모양을 직접 그려서 사용하려고 하였으나,
이미지를 pixel단위로 처리하는 CNN의 특성 상 유의미한 결과를 만들어내지 못하였음.
