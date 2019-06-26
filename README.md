# yellowtaxi
## 🚕 Жёлтое такси в Нью-Йорке. Финальный проект специализации [Машинное обучение и анализ данных](https://www.coursera.org/specializations/machine-learning-data-analysis).
- [Демонстрация результатов работы](https://www.artemklopow.ru/yellowtaxi/).  
- [Соревнование на kaggle](http://www.kaggle.com/c/yellowtaxi).

Задача проекта — научиться предсказывать количество поездок в ближайшие часы в каждом районе Нью-Йорка. Для обучения использовались данные с мая 2014г. по май 2016г. Прогнозы составлены на июнь 2016г.
Метрика качества - среднее абсолютное отклонение. Полученная ошибка - 18.745.
### Краткое описание разделов проекта.

#### [1. Знакомство с данными и агрегация](1_Data.ipynb).
Скачаны сырые данные о поездках жёлтого такси с сайта TLC: www.nyc.gov/html/tlc/html/about/trip_record_data.shtml. Данные были очищены от ошибок и аномалий.  Посчитано количество поездок за каждый час из каждой области.

#### [2. Работа с геоданными.](2_GEO_data.ipynb)
Отброшены  регионы, из которых в мае 16-го совершилось в среднем меньше 5 поездок в час. Выполнена визуализация районов Нью-Йорка на карте, с посчитанным средним количеством поездок в час в мае 16-го.

#### [3. Прогнозирование ряда со сложной сезонностью.](3_Diff_seasonality.ipynb)
По данным одного из регионов была построена модель SARIMAX.

#### [4. Прогнозирование большого количества рядов.](4_Series.ipynb)
Проведена кластеризация стандартизированных временных рядов на 5 кластеров. Для каждого кластера построена модель SARIMAX, построены прогнозы на июнь 16-го. Среднее абсолютное отклонение по итогам раздела - 29.080.

#### [5. Прогнозирование с помощью регрессии.](5_Regression.ipynb)
Построены признаки для регрессии, 6 выборок для прогнозов на 1 - 6 часов. Рассматривались модели Ridge, Lasso, XGBRegressor и нейросеть с двумя скрытыми слоями. На данных за май подобраны гиперпараметры моделей. К дальнейшему рассмотрению была принята модель XGBRegressor. Среднее абсолютное отклонение по итогам раздела - 24.085.

#### [6. Дополнительные признаки.](6_Features.ipynb)
Построены дополнительные признаки для регрессии, выброшены аномальные значения. Среднее абсолютное отклонение по итогам раздела - 18.745.

#### [7. Оформление проекта.](7_Demo.ipynb)
Сделана [демонстрация](https://www.artemklopow.ru/yellowtaxi/).
