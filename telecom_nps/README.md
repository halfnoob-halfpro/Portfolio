# Исследование опроса клиентов телекомунникацонной компании    
`SQL` `Tableau` `Постороение дашбордов` `Маркетинг-аналитик` `Продуктовый аналитик`   

## Описание проекта   

Заказчик этого исследования — большая телекоммуникационная компания, которая оказывает услуги на территории всего СНГ. Перед компанией стоит задача определить текущий уровень потребительской лояльности, или NPS (от англ. Net Promoter Score), среди клиентов из России. Чтобы определить уровень лояльности, клиентам задавали классический вопрос: «Оцените по шкале от 1 до 10 вероятность того, что вы порекомендуете компанию друзьям и знакомым». Компания провела опрос и попросила меня подготовить дашборд с его итогами. Большую базу данных для такой задачи разворачивать не стали и выгрузили данные в SQLite.

В ходе исследования ответим на следующие вопросы:

- Как распределены участники опроса по возрасту и полу?    
- Каких пользователей больше: новых или старых?    
- Пользователи из каких городов активнее участвовали в опросе?    
- Какие группы пользователей наиболее лояльны к сервису? Какие менее?    
- Какой общий NPS среди всех опрошенных?    
- Как можно описать клиентов, которые относятся к группе cторонников?    


Исследование проведем в два этапа:

- Выгрузка данных    
- Создание дашборда в Tableau    


## Описание данных

Таблица **user**    
Содержит основную информацию о клиентах.
- user_id -	Идентификатор клиента, первичный ключ таблицы
- lt_day -	Количество дней «жизни» клиента
- age -	Возраст клиента в годах
- gender_segment -	Пол клиента (1 – женщина, 0 – мужчина)
- os_name -	Тип операционной системы
- cpe_type_name -	Тип устройства
- location_id -	Идентификатор домашнего региона клиента, внешний ключ, отсылающий к таблице location
- age_gr_id -	Идентификатор возрастного сегмента клиента, внешний ключ, отсылающий к таблице age_segment
- tr_gr_id -	Идентификатор сегмента клиента по объёму потребляемого трафика в месяц, внешний ключ, отсылающий к таблице traffic_segment
- lt_gr_id -	Идентификатор сегмента клиента по количеству месяцев «жизни», внешний ключ, отсылающий к таблице lifetime_segment
- nps_score -	Оценка клиента в NPS-опросе (от 1 до 10)


Таблица **location**    
Справочник территорий, в которых телеком-компания оказывает услуги.
- location_id -	Идентификатор записи, первичный ключ
- country -	Страна
- city -	Город


Таблица **age_segment**    
Данные о возрастных сегментах клиентов.
- age_gr_id -	Идентификатор сегмента, первичный ключ
- bucket_min -	Минимальная граница сегмента
- bucket_max -	Максимальная граница сегмента
- title -	Название сегмента


Таблица **traffic_segment**    
Данные о выделяемых сегментах по объёму потребляемого трафика.
- tr_gr_id -	Идентификатор сегмента, первичный ключ
- bucket_min -	Минимальная граница сегмента
- bucket_max -	Максимальная граница сегмента
- title -	Название сегмента


Таблица **lifetime_segment**    
Данные о выделяемых сегментах по количеству месяцев «жизни» клиента — лайфтайму.
- lt_gr_id -	Идентификатор сегмента, первичный ключ
- bucket_min -	Минимальная граница сегмента
- bucket_max -	Максимальная граница сегмента
- title -	Название сегмента

## Используемые библиотеки:
`os` `pandas` `numpy` `sqlalchemy`
