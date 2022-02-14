# Credit Scoring

Проект был выполнен на платформе kaggle.com в рамках соревнования [Credit Scoring](https://www.kaggle.com/c/sf-dst-scoring)

## Цeли и задачи проекта:
**Цель проекта:** 
Построить скоринговую модель для будущих клиентов банка, которая бы предсказывала вероятность невозврата кредита. 

## Краткая информация о данных:
Исходный набор данных содержит:

- Анкетная информация по 73799 клиентам  и факт наличия дефолта у них
- Условия проживания описаны в виде 6 номинативных признаков и 13 (включая наличие дефолта) количественных признаков.
- Количественные признаки практически не содержат выбросов.
- Только один из признаков содержит пропуски.


### Этапы работы:
- Определены вспомогательные функций
- Загружен учебный датасет 100000 строк 19 признаков
- Проведен анализ данных
- Заполнены пустые значения с учетом других признаков 
- Признаки перекодированы, объединены, прологарифмированы
- Проведена проверка на значимость колличественных переменныx
	- Очистка от признаков, в которых не найдены статистически значимые различия 
- Проведен корреляционный анализ для количественных признаков
	- Очистка данных от признаков с высоким коээфициентом корреляции  
- Подготовка данных для модели:
    - Стандартизация числовых признаков
    - OneHotEncoding подход к категориальным признакам
    - Разбиение на тестовую и валидационную выборку
	- Добавлены несколько новых признаков

- Построены модели LogisticRegression, с оценкой качества модели по ROC-AUС
	- Определение оптимальных гиперпарамтров для модели
- Проведена балансировка выборки - undersampling и oversampling методами
- Выбор наилучшей модели
- Подведение итогов

Точность предсказания для модели дефолта: ROC-AUС = **0.739**.

## Набрано баллов - 24/24

## Ответы на вопросы саморефлексии:
1. **Какова была ваша роль в команде?** 
- Создать команду не удалось. 

2. **Какой частью своей работы вы остались особенно довольны?** 
 Оформление и постороение графиков.

3. **Что не получилось сделать так, как хотелось? Над чем ещё стоит поработать?** 
 - Написать больше универсальных функций. Future Engeneering, не испытал множество задуманных фич.

4. **Что интересного и полезного вы узнали в этом модуле?** 
 - Самостоятельно поработал с моделью логистической регрессии, подбирал гипертаматры для нее. 

5. **Что является вашим главным результатом при прохождении этого проекта?** 
 - Получил практику построения моделей. 

6. **Какие навыки вы уже можете применить в текущей деятельности?** 
 - EDA и LogisticRegression.

7. **Планируете ли вы дополнительно изучать материалы по теме проекта?** 
 - изучу Plotly, понравились графики.
