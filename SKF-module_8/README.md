# CarPricePrediction  NLP + MLP + CNN

Проект был выполнен на платформе kaggle.com в рамках соревнования [ Car Price prediction Part2](https://www.kaggle.com/c/sf-dst-car-price-prediction-part2)

## Цeли и задачи проекта:
**Цель проекта:** 
Построить модель прогнозирование стоимости автомобиля по табличным данным, описаниям к автомобилю, и его фотографий  полученныx с сайта auto.ru.   
Построить multi-input нейронную сеть.
Для оценки точности цены использовать метрику MAPE. 

## Краткая информация о данных:
Данные представляют собой описание автомобилей в виде табличных данных, текстового описания (признак 'description') и изображение автомобиля
Обучающая выборка состоит из 6682 примеров
Тестовая выборка состоит из 1671 примера

## Реализация:

- Анализ данных
- Предобработка данных:
  - приведение кодировок к единому формату, заменены ошибки
  - проведено логарифмирование признаков и нормализация
  - удалены записи с специфичными автомобилями (электрокары, лимузины)
  - подготовлены дополнительные признаки из описания и комбинации числовых
  - часть признаков удалена, на основе анализа корреляции
  - была произведена лемматизация текста в признаке 'description' с последующей и токенизацией
  - Label Encoding, One-Hot Encoding, HelmertEncoder
- проверено несколько вариантов архитектуры сети для обработки табличных данных
- настройка callback
- опробованы архитектуры сети для обработки текстовых данных, в том числе мультиязычный BERT
- применены сложные и простые аугментации на основе библиотеки albumentation
- обучение изображений на основе сетей EfficientNetB3, EfficientNetV2M
- Multi-input нейронная сеть для анализа табличных данных, текста и фотографий одновременно
- несколько вариантов ансамблей моделей

## Итоги обучения:

CatBoost---------------------10.53%  
MLP--------------------------11.47%  
MLP + NLP--------------------16.12%  
MLP + NLP + CNN--------------17.19%  
NLP--------------------------53.09%  
CNN--------------------------48.86%  
Blend CatBoost и MLP---------10.23%  
Blend CatBoost и MLP_NLP_CNN-12.48%  
Метрика MAPE ,на соревновании kaggle равна 11.18687 % (40-е место).

## Набрано баллов: 33/33



