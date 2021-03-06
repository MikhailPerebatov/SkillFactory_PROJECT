# Car Price prediction
## Прогнозирование стоимости автомобиля по характеристикам


Проект был выполнен на платформе kaggle.com в рамках соревнования [Car Price prediction](https://www.kaggle.com/c/sf-dst-car-price-prediction)

## Цeли и задачи проекта:
**Цель проекта:** 
Построить модель прогнозирования стоимости автомобиля по характеристикам полученным с сайта auto.ru. 
Для оценки использовать метрику MAPE.

## Краткая информация о данных:
Исходный набор данных содержит:

- Анкетная информация по 73799 клиентам  и факт наличия дефолта у них
- Условия проживания описаны в виде 6 номинативных признаков и 13 (включая наличие дефолта) количественных признаков.
- Количественные признаки практически не содержат выбросов.
- Только один из признаков содержит пропуски.

### Этапы работы:
- Парсинг;
- EDA, Предобработка
- Заполнены пустые значения с учетом других признаков 
- Признаки перекодированы, объединены, прологарифмированы
- Проведена проверка на значимость колличественных переменныx
	- Очистка от признаков, в которых не найдены статистически значимые различия 
- Проведен корреляционный анализ для количественных признаков
	- Очистка данных от признаков с высоким коээфициентом корреляции  
- Подготовка данных для модели:
    - OneHotLabels
    - OneHotEncoding подход к категориальным признакам
    - Разбиение на тестовую и валидационную выборку
	- Добавлены несколько новых признаков
- Model
  - Наивная модель(median)
  - CatBoost
  - RandomForest
  - LinerRegression
  - GradientBoosting
  - LGBMRegressor
  - Ансамбль моделей Stacking (LGBMRegressor+ GradientBoostingRegressor meta - LinerRegression)
- Выбор наилучшей модели
- Подведение итогов

Точность предсказания для модели авто: MAPE = **13.13%**.

## Набрано баллов: 20/24 (снижена за отсутсвие команды)

## Как сделать лучше:
- Убрать фичи и признаки ухудшающие оценку.
- Убрать выбросы
- Лучше подобрать гиперепараметры к RandomForest, LGBM  
- Найти лушие варианты ансамблирования моделей, простая + сложная




