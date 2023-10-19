# Yandex-Projects
Проекты, выполненные в рамках обучения по специальности Data Scientist Plus.

## Временные ряды

<table>
<tr>
  <th>Название проекта</th>
  <th>Описание</th>
  <th>Стек</th>
</tr> 
  
<tr>
  <td><a href = "https://github.com/Vanarty/Yandex-Projects/tree/main/machine_learning/taxi_orders">Прогнозирование заказов такси</a> (Задача регрессии)</td>
  <td> Компания «Чётенькое такси» собрала исторические данные о заказах такси в аэропортах. Чтобы привлекать больше водителей в период пиковой нагрузки, нужно спрогнозировать количество заказов такси на следующий час. Необходимо построить модель для такого предсказания.</td>
  <td>Jupyter Notebook, Python, os, pandas, numpy, sklearn, <strong>statsmodels, Prophet, TimeSeriesSplit, Pipeline, GridSearchCV, TransformerMixin, XGBRegressor, LGBMRegressor, CatBoostRegressor</strong></td>
</tr>

</table>

## Нейронные сети

<table>
<tr>
  <th>Название проекта</th>
  <th>Описание</th>
  <th>Стек</th>
</tr> 
  
<tr>
  <td><a href = "https://github.com/Vanarty/Yandex-Projects/tree/main/neural_networks">Прогнозирование температуры звезд</a> (Задача регрессии)</td>
  <td> Задача от обсерватории «Небо на ладони»: придумать, как с помощью нейросети определять температуру на поверхности обнаруженных звёзд по известным признакам.</td>
  <td>Jupyter Notebook, Python, os, pandas, numpy, seaborn, sklearn, <strong>Pytorch, Skorch, PCA</strong></td>
</tr>

</table>

## Классическое машинное обучение

<table>
<tr>
  <th>Название проекта</th>
  <th>Описание</th>
  <th>Стек</th>
</tr> 
  
<tr>
  <td><a href = "https://github.com/Vanarty/Yandex-Projects/tree/main/machine_learning/car_accident_risk">Оценка риска ДТП</a> (Задача классификации)</td>
  <td> Нужно создать систему для каршеринговой компании, которая могла бы оценить риск ДТП по совокупности факторов. Как только водитель забронировал автомобиль, сел за руль и выбрал маршрут, система должна оценить уровень риска. Если уровень риска высок, водитель увидит предупреждение и рекомендации по маршруту.</td>
  <td>Jupyter Notebook, Python, pandas, numpy, seaborn, sklearn, <strong>sqlalchemy, Shap, Pipeline, Preprocessing, LogisticRegression, RandomForestClassifier, XGBClassifier, CatBoostClassifier, LGBMClassifier</strong></td>
</tr>
<tr>
  <td><a href = "https://github.com/Vanarty/Yandex-Projects/tree/main/machine_learning/car_price_predict">Предсказание стоимости автомобилей</a> (Задача регрессии)</td>
  <td> Сервис по продаже автомобилей с пробегом «Не бит, не крашен» разрабатывает приложение для привлечения новых клиентов. Необходимо построить модель для предсказания стоимости авто.</td>
  <td>Jupyter Notebook, Python, pandas, numpy, seaborn, sklearn, <strong>Pipeline, TransformerMixin, DecisionTreeRegressor, RandomForestRegressor, XGBRegressor, LGBMRegressor, CatBoostRegressor</strong></td>
</tr>
<tr>
  <td><a href = "https://github.com/Vanarty/Yandex-Projects/tree/main/machine_learning/personal_data_protection">Защита персональных данных клиентов</a> (Задача регрессии)</td>
  <td> Необходимо защитить данные клиентов страховой компании «Хоть потоп». Разработаем такой метод преобразования данных, чтобы по ним было сложно восстановить персональную информацию. Обоснуем корректность его работы.</td>
  <td>Jupyter Notebook, Python, pandas, numpy, seaborn, sklearn, <strong> Pipeline, Preprocessing, PolynomialFeatures, LinearRegression, Lightgbm</strong></td>
</tr>
<tr>
  <td><a href = "https://github.com/Vanarty/Yandex-Projects/tree/main/machine_learning/spark_house_price_predict">Предсказание стоимости жилья в Калифорнии</a> (Задача регрессии)</td>
  <td> В проекте необходимо обучить модель линейной регрессии на данных о жилье в Калифорнии в 1990 году используя фреймворк Spark для распределённых вычислений.</td>
  <td>Jupyter Notebook, Python, pandas, numpy, seaborn, <strong>Pyspark, Pipeline, StringIndexer, VectorAssembler, StandardScaler, LinearRegression, RegressionEvaluator, ParamGridBuilder, CrossValidator</strong></td>
</tr>
<tr>
  <td><a href = "https://github.com/Vanarty/Yandex-Projects/tree/main/machine_learning/hotel_customer_churn">Прогнозирование оттока клиентов в сети отелей</a> (Задача классификации)</td>
  <td> Заказчик исследования — сеть отелей «Как в гостях». Чтобы привлечь клиентов, сеть отелей добавила на свой сайт возможность забронировать номер без предоплаты. Однако если клиент отменяет бронирование, то компания терпит убытки. Чтобы решить эту проблему, нам нужно разработать систему, которая предсказывает отказ от брони. Если модель покажет, что бронь будет отменена, то клиенту предлагается внести депозит.</td>
  <td>Jupyter Notebook, Python, pandas, numpy, seaborn, <strong>plotly, eli5, Preprocessing, GridSearchCV, Pipeline, DecisionTreeClassifier RandomForestClassifier, LogisticRegression, XGBClassifier</strong></td>
</tr>
<tr>
  <td><a href = "https://github.com/Vanarty/Yandex-Projects/tree/main/machine_learning/oil_well_location">Выбор локации для скважины</a> (Задача регрессии)</td>
  <td> Мы работаем в добывающей компании «ГлавРосГосНефть». Нужно решить, где бурить новую скважину.</td>
  <td>Jupyter Notebook, Python, pandas, numpy, seaborn, <strong>scipy, LinearRegression</strong></td>
</tr>
<tr>
  <td><a href = "https://github.com/Vanarty/Yandex-Projects/tree/main/machine_learning/bank_customer_churn">Отток клиентов</a> (Задача классификации)</td>
  <td>Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых. Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет.</td>
  <td>Jupyter Notebook, Python, pandas, numpy, seaborn, <strong>scipy, Preprocessing, SMOTE, DecisionTreeClassifier, RandomForestClassifier, LogisticRegression</strong></td>
</tr>
<tr>
  <td><a href = "https://github.com/Vanarty/Yandex-Projects/tree/main/machine_learning/tariff_prediction">Рекомендация тарифов</a> (Задача классификации)</td>
  <td>Оператор мобильной связи «Мегалайн» выяснил: многие клиенты пользуются архивными тарифами. Они хотят построить систему, способную проанализировать поведение клиентов и предложить пользователям новый тариф: «Смарт» или «Ультра».</td>
  <td>Jupyter Notebook, Python, pandas, numpy, seaborn, <strong>GridSearchCV, DecisionTreeClassifier, RandomForestClassifier, LogisticRegression, KNeighborsClassifier</strong></td>
</tr>

</table>
</details>

## Исследовательский анализ данных (EDA)

<table>
<tr>
  <th>Название проекта</th>
  <th>Описание</th>
  <th>Стек</th>
</tr> 
  
<tr>
  <td><a href = "https://github.com/Vanarty/Yandex-Projects/tree/main/analytics_eda/research_the_sale_of_apartments">Исследование объявлений о продаже квартир</a></td>
  <td> В нашем распоряжении данные сервиса Яндекс.Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет. Нужно научиться определять рыночную стоимость объектов недвижимости. Ваша задача — установить параметры. Это позволит построить автоматизированную систему: она отследит аномалии и мошенническую деятельность. По каждой квартире на продажу доступны два вида данных. Первые вписаны пользователем, вторые — получены автоматически на основе картографических данных. Например, расстояние до центра, аэропорта, ближайшего парка и водоёма..</td>
  <td>Jupyter Notebook, Python, pandas, numpy, matplotlib</td>
</tr>

</table>
