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

11가지 음식 별 input 이미지 데이터 카테고리 분류 유사도 측정 결과 각 카테고리 별 유사도(거리)는 큰 차이는 없었다.

이는 row데이터 사물의 픽셀값은 균일하나 프레임 내 사물의 위치 좌표 및 객체가 전체 크기에 차지하는 비율에 영향을 받는 것으로 보인다.

하지만 중앙에 2:1 정도의 이미지에서 TOP1 카테고리의 정확도는 높은 성능을 보여 성능 개선을 위해 이미지 리사이징에 대한 고찰이 필요할 것으로 판단된다. 
