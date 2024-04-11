# chromadb_ViT_food

총 11종의 음식 이미지 분류를 위한 chromad 내 DINO-ViT-S/16 모델 적용 

<img src="image/result_food_meat.png">
<img src="image/result_food_soup.png">


<br /><br /> 
## Object

DINO-ViT-S/16 모델은 DINO 방법을 사용하여 훈련된 ViT 모델로 224x224 픽셀의 해상도에서 ImageNet-1k 라는 대규모 이미지 컬렉션에 

사전 학습된 변환기 인코더 모델입니다. 사전 훈련된 모델은 다운스트림 작업에 유용한 기능을 추출하는 데 사용할 수 있는 이미지의 내부 

표현을 학습합니다. 본 과정에서 Kaggle의 Food-11 image dataset을 활용하여 11가지 주요 음식 카테고리로 분류된 16643개의 음식 이미지를

학습하고 입력된 이미지의 카테고리 분류 및 유사도를 측정하는 모델 제작을 목표로 합니다.

<br /><br /> 
## Dataset

- Food-11 image dataset

<br /><br /> 
## Libraries used

- Transformers_DINO-ViT-S/16
- PIL_Image
- chromadb

<br /><br /> 

## Result

11가지 음식에 대한 입력 이미지 데이터의 카테고리 분류 유사도 측정 결과, 각 카테고리 간의 유사도(거리)는 큰 차이를 보이지 않았습니다.

이러한 결과는 이미지의 픽셀값이 균일하지만, 프레임 내에 있는 객체의 위치 및 크기가 전체 이미지에 차지하는 비율에 영향을 받기 때문으로 판단됩니다.

더불어 중앙에 위치한 2:1 비율의 이미지에서는 TOP-5 카테고리에 대한 분류 정확도는 준수한 성능을 보였습니다.

이러한 성능 비교 결과를 통해 입력 데이터의 리사이징은 성능 개선을 위한 중요한 고려 사항이 될 수 있을 것입니다.
