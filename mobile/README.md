
# Анализ поведения пользователей мобильного приложения
`Python` `Pandas` `Matplotlib` `Seaborn` `Plotly` `SciPy` `Проверка статистических гипотез`

## Описание проекта   

Целью исследования является изучение основных паттернов поведения пользователей мобильного приложения и определение характерных сценариев, которые приводят к совершению пользователем целевого действия - просмотра контактов.    
Исследование проводится на основе датасета, содержащего данные о событиях, совершенных в мобильном приложении
"Ненужные вещи". В нем пользователи продают свои ненужные вещи, размещая их на доске объявлений.
В датасете содержатся данные пользователей, впервые совершивших действия в
приложении после 7 октября 2019 года.

**Основные этапы исследования:**
- Предобработка данных
- Исследовательский анализ данных
- Расчёт продуктовых метрики для оценки пользовательской активности
- Анализ сценариев активности пользователей
- Проверка гипотез

## Описание данных

Таблица **mobile_sources.csv** содержит информацию об итсочниках установки пользователями приложения.

- `userId` — идентификатор пользователя,
- `source` — источник, с которого пользователь установил приложение.

Таблица **mobile_dataset.csv** содержит информацию об активности пользователей приложения.

- `event.time` — время совершения, 
- `user.id` — идентификатор пользователя,
- `event.name` — действие пользователя. Виды действий:
    - advert_open — открыл карточки объявления,
    - photos_show — просмотрел фотографий в объявлении,
    - tips_show — увидел рекомендованные объявления,
    - tips_click — кликнул по рекомендованному объявлению,
    - contacts_show и show_contacts — посмотрел номер телефона,
    - contacts_call — позвонил по номеру из объявления,
    - map — открыл карту объявлений,
    - search_1 — search_7 — разные действия, связанные с поиском по сайту,
    - favorites_add — добавил объявление в избранное. 

## Используемые библиотеки:
`pandas` `numpy` `matplotlib` `seaborn` `warnings` `scipy` `datetime` `tqdm` `plotly` `math` `statistics`