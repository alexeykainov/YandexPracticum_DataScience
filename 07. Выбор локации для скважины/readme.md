# Выбор локации для скважины

## Описание проектной работы

Для добывающей компании «ГлавРосГосНефть» необходимо решить где бурить новую скважину.

Предоставлены пробы нефти в трёх регионах: в каждом 10 000 месторождений, где измерили качество нефти и объём её запасов. 

## Цель проекта

Необходимо построить модель машинного обучения, которая поможет определить регион, где добыча принесёт наибольшую прибыль. Проанализировать возможную прибыль и риски техникой `Bootstrap`.

## Условия задачи

- для обучения модели подходит только линейная регрессия (остальные — недостаточно предсказуемые)
- при разведке региона исследуют 500 точек, из которых с помощью машинного обучения выбирают 200 лучших для разработки
- бюджет на разработку скважин в регионе — 10 млрд рублей
- при нынешних ценах один баррель сырья приносит 450 рублей дохода. Доход с каждой единицы продукта составляет 450 тыс. рублей, поскольку объём указан в тысячах баррелей
- после оценки рисков нужно оставить лишь те регионы, в которых вероятность убытков меньше `2.5%`. Среди них выбирают регион с наибольшей средней прибылью.

## Описание данных

- `id` - уникальный идентификатор скважины
- `f0, f1, f2` - три признака точек (неважно, что они означают, но сами признаки значимы)
- `product` - объём запасов в скважине (тыс. баррелей)

## Ход выполнения работы

- изучение общей информации
- обучение и проверка моделей для каждого региона, расчёт среднего запаса предсказанного сырья и `RMSE` модели
- расчёт прибыли, расчёт достаточного объёма сырья для безубыточной разработки новой скважины
- разработка функции для расчёта прибыли по выбранным скважинам и предсказаниям модели
- расчёт рисков и прибыли для каждого региона, определение распределения прибыли для `1000` выборок. Расчёт средней прибыли, `95%`-ого доверительного интервала и риска убытков.
- общие выводы

## Сферы деятельности компаний

- **Добывающие компании**

## Направление деятельности

- **Машинное обучение**
- **Регрессия**
- **Разработка бизнес-модели**
- **Финансовый аналитик**

## Навыки и инструменты

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Sklearn**
- **Seaborn**
- **Ridge**
- **GridSearchCV**
- **StandardScaler**
- **Bootstrap**

## Выводы

Проанализировал данные геологоразведки для трёх регионов. Обучил три модели для предсказания запасов сырья для трех регионов. Вычислил минимально-необходимый средний запас сырья для безубыточной разработки новых скважин. Рассчитал риски и прибыль для каждого региона. Определил, что `второй регион` является самым потенциально-значимым для разработки, т.к. получил самый низкий риск убытков `1.4%`. 
