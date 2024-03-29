**﻿Цели проекта**

Целью работы является выявление модели, позволяющей прогнозировать отток клиентов банка со значением f1-меры не менее 0.59%.

Описание данных:

Признаки
 - RowNumber — индекс строки в данных
 - CustomerId — уникальный идентификатор клиента
 - Surname — фамилия
 - CreditScore — кредитный рейтинг
 - Geography — страна проживания
 - Gender — пол
 - Age — возраст
 - Tenure — сколько лет человек является клиентом банка
 - Balance — баланс на счёте
 - NumOfProducts — количество продуктов банка, используемых клиентом
 - HasCrCard — наличие кредитной карты
 - IsActiveMember — активность клиента
 - EstimatedSalary — предполагаемая зарплата
 
Целевой признак
 - Exited — факт ухода клиента


**Используемые модели**

 - Дерево решений
 - Случайный лес

Для борьбы с дисбалансом использовались методы:
 - Взвешивание классов через гиперпараметры моделей
 - Увеличение выборки
 - Уменьшение выборки

Самые высокие значения f1 меры получились у модели случайного леса при использовании весов классов. 

**Заключение**

В качестве модели для прогноза оттока клиентов лучшие результаты показал алгоритм случайного леса с гиперпараметрами:
 - глубина дерева - 8, 
 - вес класса - 'balanced',
 - число признаков для разделения - 1,
 - количество деревьев - 60 и 
 - порог классификации - 0,52.

Модель позволяет достичь значение f1-меры в 0.5993 на валидационной выборке и 0.6093 - на тестовой.



