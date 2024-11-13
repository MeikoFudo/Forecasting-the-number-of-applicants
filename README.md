# Проект: Анализ и кластеризация пользователей с использованием данных Яндекс.Метрики

## Описание

Этот проект включает в себя серию ноутбуков, направленных на анализ данных с Яндекс.Метрики, их кластеризацию и классификацию с использованием моделей машинного обучения, таких как XGBoost. Данные используются для сегментации пользователей и предсказания их поведения на основе различных метрик посещаемости сайта.

### Структура проекта:

- **Uploading_Data.ipynb**: Код для выгрузки данных с Яндекс.Метрики с использованием API.
- **trying-to-cluster-the-unclustered.ipynb**: Проверка гипотез по кластеризации всех пользователей разом.
- **classification-by-cluster.ipynb**: Кластеризация пользователей, относящихся к категории "postuplenie".
- **clusters-postuplenie.ipynb**: Модель XGBoost для классификации пользователей по кластерам.

## Как использовать

### 1. Выгрузка данных с Яндекс.Метрики

Для начала работы с проектом, необходимо выгрузить данные с Яндекс.Метрики. В ноутбуке **Uploading_Data.ipynb** реализована выгрузка с использованием следующего кода:

```python
dimensions = 'ym:s:date,ym:s:ipAddress,ym:s:visitDuration,ym:s:isNewUser,ym:s:daysSinceFirstVisit,ym:s:userVisitsPeriod,ym:s:previousVisitDate,ym:s:ageInterval,ym:s:regionArea,ym:s:userVisits'
metrics = 'ym:s:bounceRate,ym:s:pageDepth,ym:s:avgVisitDurationSeconds,ym:s:pageviews'
```
Ссылка на датасет с пользователями, которые интересовались поступлением и с кластерами в качестве меток: https://github.com/MeikoFudo/Forecasting-the-number-of-applicants 

![xgboost_tree](https://github.com/user-attachments/assets/922f6638-fb38-4da8-9519-d2f153bcbe81)
![image](https://github.com/user-attachments/assets/04a80b57-b492-406d-8e1a-f2f9a51f4c7b)
