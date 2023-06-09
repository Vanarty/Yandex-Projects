# Предсказание сердечно-сосудистых заболеваний.
Онлайн приложение доступно по адресу: https://heart-diseases-prediction.streamlit.app/

* Автор проекта - *Иванов Артём Юрьевич*
* vanarty@yandex.ru

## 1. Описание проекта

### 1.1. Задача: 
- Построить модель, предсказываюшую вероятность (**риск**) *сердечно-сосудистых заболеваний (ССЗ)* на основе входных данных о пациенте.
- Развернуть приложение на базе **`Streamlit`** с возможностью ввода пользователем собственных данных для получения прогноза вероятности *ССЗ*.
- (*Дополнительно*): в случае прогнозирования **высокого риска** *ССЗ* указать пользователю какие **факторы** создают наибольший риск.

### 1.2. Входные данные 

Данные для обучения модели были взяты с общедоступной базы на **Kaggle**.

Ссылка: https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset

В данном проекте данные разбиты по следующим файлам:
- train.csv (размер: 70000 записей, 12 признаков);
- test.csv (размер: 70000 записей, 11 признаков).

В обучающих данных (`train.csv`) один из признаков является целевым (колонка *`cardio`*) и является бинарным призанком (**1 - пациент имеет ССЗ, 0 - не имеет**)

Для обучения модели доступны следующие признаки:
- `age` | возраст пациента | тип данных: int | количественный признак
- `height` | рост пациента | тип данных: int | количественный признак
- `weight` | вес пациента | тип данных: float | количественный признак
- `gender` | пол пациента | categorical code | бинарный признак
- `ap_hi` | верхнее (систолическое) давление | тип данных: int | количественный признак
- `ap_lo` | нижнее (диастолическое) давление | тип данных: int | количественный признак
- `cholesterol` | уровень холестерина | тип данных: int | категориальный признак
- `gluc` | уровень глюкозы | тип данных: int | категориальный признак
- `smoke` | показатель того, курит ли пациент | тип данных: int | бинарный признак
- `alco` | показатель того, употребляет ли пациент алкоголь | бинарный признак
- `active` | показатель того, ведет ли пациент какую-либо доп. физическую активность | тип данных: int | бинарный признак

### 1.3 Оработка данных, создание дополнительных признаков, модель

Перед обучением моделей данные были обработаны. В частности обработаны значения признаков `ap_hi` и `ap_lo` (изменен масштаб значений, исправлены взаимно-перекрестные значения). Так же отмасштабирован признак `age` изначально выраженных в `'днях'`. Для этого был создан новый признак `years`, где значения указаны в `'годах'`.

Проведен **Feature Enginiring**. Были созданы признаки на соснове имеющихся, а так же проанализрованы распределения двух групп пациентов по таргету (признаку `cardio`) в разрезе этих признаков для определения степени их значимости для прогностической способности будущей модели. Признаки:
- `mass_idx` | индекс массы тела | тип данных: int | количественный признак
- `avrg_up` | среднее артериальное давление | тип данных: float | количественный признак
- `aphi_chol_gluc` | индекс "ср.давление+возраст x сахар+холестерин" | тип данных: int | количественный признак
- `life_st` | степень качества жизни | тип данных: int | категориальный признак
- `ag_st` | степень артериального давления | тип данных: int | категориальный признак
- `ssz_risc` | степень риска ССЗ с учетом признаков `aphi_chol_gluc`, `years` и `aphi_chol_gluc` | тип данных: int | количественный признак.

Для обучения были выбраны 3 модели с дефолтными параметрами: **RandomForestClassifier**, **LogisticRegression** и **XGBClassifier**. Для оценки модели была выбрана метрика **ROC_AUC**. Лучший результат показала модель **XGBClassifier**.

Далее с помощью `'GridSearchCV'` были подобраны лучшие гиперпараметры для модели **XGBClassifier**.  Модель сохранена в файл в формате *`pickle`*.

Для определения важности признаков и их влияния на целевой признак был использован **Shap**. Наиболее важными для предсказания признаками в порядке убывания важности являются: `ap_hi`, `ssz_risc`, `age`, `cholesterol`, `aphi_chol_gluc`, `avrg_ap`, `mass_idx`.

В рамках (дополнительнгой) работы был так же применен **PCA** (анализ первичных компонент) на обучающих данных. Но он не дал ощутимых результатов.

### 1.4 Создание приложения на базе Streamlit

На основе **Streamlit** было создано приложение для пользователей, которое основывваясь на лучшей модели **XGBClassifier** предсказывает вероятность (риск) наличия сердечно-сосудистых заболеваний.

Техническая справка для ипользования:
- файл программы (на англ.языке) расположен в папке `'/Streamli prod/'`;
- название файла программы `'app_en.py'`;
- версия `Streamlit` - 1.19.0

Функции программы:
- предсказание в `%` вероятности (риска) наличия ССЗ;
- указание факторов риска, которые могут быть причинами ССЗ.

--------

- в версии 1.1 добавлена русская версия программы

### Ссылка на проект (Githab):

https://github.com/Vanarty/Heart-diseases-prediction-kaggle-/commits/master
