# Исследование активности пользователей Википедии
`Python` `Pandas` `Matplotlib` `Seaborn` `Plotly` `RFM`

## Описание проекта   

В нашем распоряжении данные о пользовтаелях и выборах в Википедии.На основе этих данных мы проведём анализ активности пользователей, выявим их
предпочтения, сделаем сегментацию, выясним кто такой типичный пользователь.    

**Цель проекта:**    
- Изучить данные, привести их в пригодный для анализа формат.
- Обнаружить в них значимые инсайты.
- Исследовать голосующую аудиторию проекта.
- Разделить пользователей на сегменты и изучить данные подробнее в разрезе сегментов.

**Этапы исследования:**
- Исследование данных о голосованиях
- Исследование данных о пользователях
- Исследование агрегированных данных


## Описание данных

Таблица  **stats** содержит информацию о пользователях    
- Edits - Количество правок    
- Reverts - Количество отмен чужих правок    
- Log - Количество иных действий    
- Diff - Добавленное минус удалённое    
- Volume - Общий объём добавленного    
- Tot size - Накопленная сумма добавленного    
- Time - Время онлайн    
- Speed - Скорость (количество правок в единицу времени)    
- User - Ник пользователя    
- txt - Дата в текстовом формате    

Таблица **votes** содержит информацию о голосовании
- voter - Голосующий    
- can_vote - Проходит по критериям    
- time - Время голоса    
- candidate - Кандидат, по которому голос    
- n - Номер выборов, с дробными частями - довыборы    
- vote - Голос, 1 - за, -1 - против    
- lt - Суток от начала текущих выборов    

## Используемые библиотеки:
`pandas` `numpy` `matplotlib` `seaborn` `plotly` `datetime` `math`

