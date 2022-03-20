# Service_Out_Prediction
## Telco-Customer-Churn data를 통해 고객의 서비스 해지 여부를 예측한다.
고객 서비스 해지 여부를 예측하는 것으로, 각 고객별 다양한 특성들을 기반으로 binary classifcation을 진행하였다. 데이터 전처리는 Label Encoding, normalization, 결측값 대체, 불필요한 feature 제거 등으로 이루어졌다. 데이터의 선형성 여부를 비교하기 위해 Logistic Regression, MLP, RandomForest의 세 모델을 사용하였다. 실험은 feature selection을 하지 않은 상태와 featue selection을 모델 기반 특성 선택과, 반복적 특성 선택 두가지 방식을 진행한 후에 GidSerachCV를 이용해 최적화 모델을 생성하여 진행하였다. 이 데이터는 class가 imbalanced 되어있기 때문에 성능을 accuracy만으로 판단하기 힘들어 confusion matrix, f1_score, ROC, AUC 등을 활용하여 성능 비교 분석을 진행하였다.


실험 분석 결과, 세가지 실험(no feature selection, model based feature selection, iterative feature selection)에서 Logistic Regression이 평균적으로 가장 높은 성능을 보여주었다. 그리고 RandomForest 모델의 경우는 model based feature selection 이후 상대적으로 큰 성능 향상을 보여주었다. 그리고 feature의 수를 19개에서 15개, 10개로 줄여가며 진행했을 때, 10개로 줄였을 때 나머지 두 모델과는 달리 MLP는 AUC 측면에서의 성능 향상을 보여주었다. 
