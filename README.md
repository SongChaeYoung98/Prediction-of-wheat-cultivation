# prediction-of-wheat-cultivating-areas
한국의 밀 재배 가능 지역 예측

## Language, Development tools
Python 3, Jyputer Notebook

## Main Dependencies
- Scikit-Learn
- Pandas
- Numpy
- KNeighborsClassifier
- DecisionTreeClassifier
- StandardScaler
- RandomForestClassifier

## Predictive accuracy
- RandomForest : 0.9478
- KNN : 0.9351
- KNN Scaler : 0.9469

## Introduction
- 2020년 기후 중 지역 별 최고, 최저, 평균 기온과 강수량을 이용하여 4가지 조건에 각각 0, 1을 부여 후 최종 라벨링으로 가중치를 적용시켜 0~4 사이의 라벨링이 적용되도록 함 (0:재배불가 4:최적)
<br />(가중치가 미적용된 라벨로 학습할 경우, 과학습이 발생해 정확도가 0.9998로 나오는 현상이 발생)
- 가중치가 적용된 가공한 2020년 데이터를 학습 후 기상청에서 제공한 2030, 2040 기후 변화 정보를 기반으로 직접 가공한 미래 기후 데이터로 2030, 2040년의 기후에도 재배 가능한 대한민국 지역을 파악하는 프로그램
- 최종 분석 결과는 예측-randomforest.csv 파일 중 '라벨링' 셀에 출력, 시각화 미지원
- 2040년은 부정확한 데이터로 인해 원하는 결과가 제대로 출력되지 않음
