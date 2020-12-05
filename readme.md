**Определение перспективного тарифа для телеком компании**

В нашем распоряжении данные компании «Мегалайн» — федерального оператора сотовой связи.

*Бизнес-проблема:*

Клиентам предлагают два тарифных плана: «Смарт» и «Ультра». Чтобы скорректировать рекламный бюджет, коммерческий департамент хочет понять, какой тариф приносит больше денег. Вам предстоит сделать предварительный анализ тарифов на небольшой выборке клиентов. В нашем распоряжении данные 500 пользователей «Мегалайна»: кто они, откуда, каким тарифом пользуются, сколько звонков и сообщений каждый отправил за 2018 год. Нужно проанализировать поведение клиентов и сделать вывод — какой тариф лучше. 

*Описание тарифов:*

Тариф «Смарт»: Ежемесячная плата: 550 рублей Включено 500 минут разговора, 50 сообщений и 15 Гб интернет-трафика Стоимость услуг сверх тарифного пакета: минута разговора: 3 рубля сообщение: 3 рубля 1 Гб интернет-трафика: 200 рублей
Тариф «Ультра» Ежемесячная плата: 1950 рублей Включено 3000 минут разговора, 1000 сообщений и 30 Гб интернет-трафика Стоимость услуг сверх тарифного пакета: минута разговора: 1 рубль сообщение: 1 рубль 1 Гб интернет-трафика: 150 рублей Нужно обратить внимание: «Мегалайн» всегда округляет вверх значения минут и мегабайтов. Если пользователь проговорил всего 1 секунду, в тарифе засчитывается целая минута.

*Описание данных:*

**Таблица users (информация о пользователях):**
user_id — уникальный идентификатор пользователя
first_name — имя пользователя
last_name — фамилия пользователя
age — возраст пользователя (годы)
reg_date — дата подключения тарифа (день, месяц, год)
churn_date — дата прекращения пользования тарифом (если значение пропущено, то тариф ещё действовал на момент выгрузки данных)
city — город проживания пользователя
tariff — название тарифного плана 

**Таблица calls (информация о звонках):**
id — уникальный номер звонка
call_date — дата звонка
duration — длительность звонка в минутах
user_id — идентификатор пользователя, сделавшего звонок 

**Таблица messages (информация о сообщениях):**
id — уникальный номер сообщения
message_date — дата сообщения
user_id — идентификатор пользователя, отправившего сообщение 

**Таблица internet (информация об интернет-сессиях):**
id — уникальный номер сессии
mb_used — объём потраченного за сессию интернет-трафика (в мегабайтах)
session_date — дата интернет-сессии
user_id — идентификатор пользователя 

**Таблица tariffs (информация о тарифах):**
tariff_name — название тарифа
rub_monthly_fee — ежемесячная абонентская плата в рублях
minutes_included — количество минут разговора в месяц, включённых в абонентскую плату
messages_included — количество сообщений в месяц, включённых в абонентскую плату
mb_per_month_included — объём интернет-трафика, включённого в абонентскую плату (в мегабайтах)
rub_per_minute — стоимость минуты разговора сверх тарифного пакета (например, если в тарифе 100 минут разговора в месяц, то со 101 минуты будет взиматься плата)
rub_per_message — стоимость отправки сообщения сверх тарифного пакета
rub_per_gb — стоимость дополнительного гигабайта интернет-трафика сверх тарифного пакета (1 гигабайт = 1024 мегабайта)

*План действий:* 
1. Изучение общей информации о файле с данными
2. Предобработка данных 
3. Исследовательский анализ на основе данных
4. Статистический анализ и проверка гипотез
5. Общий вывод


**Determination of a promising tariff for a telecom company**

We have at our disposal the data of "Megaline" - a federal cellular operator.

*Business problem:*

Clients are offered two tariff plans: "Smart" and "Ultra". To adjust the advertising budget, the commercial department wants to understand which tariff brings the most money. You have to do a preliminary analysis of rates for a small sample of customers. We have at our disposal the data of 500 Megaline users: who they are, where they are from, what tariff they use, how many calls and messages each sent in 2018. It is necessary to analyze customer behavior and draw a conclusion - which tariff is better. 

*Description of tariffs:*

- "Smart" tariff: Monthly fee: 550 rubles Included 500 minutes of conversation, 50 messages and 15 GB of Internet traffic. Cost of services in excess of the tariff package: minute of conversation: 3 rubles message: 3 rubles 1 GB of Internet traffic: 200 rubles.
- Tariff "Ultra": Monthly fee: 1950 rubles Included 3000 minutes of conversation, 1000 messages and 30 GB of Internet traffic. Cost of services in excess of the tariff package: minute of conversation: 1 ruble message: 1 ruble 1 GB of Internet traffic: 150 rubles.
You should pay attention: " Megaline always rounds up the minutes and megabytes. If the user has spoken for only 1 second, the whole minute is counted in the tariff.

*Description of data:*

**Users table (information about users):**
user_id - unique user ID
first_name - username
last_name - user's last name
age - the user's age (years)
reg_date - tariff activation date (day, month, year)
churn_date - date of termination of using the tariff (if the value is omitted, then the tariff was still valid at the time of data upload)
city - user's city of residence
tariff - the name of the tariff plan

**Calls table (information about calls):**
id - unique call number
call_date - date of the call
duration - call duration in minutes
user_id - identifier of the user who made the call

**Messages table (information about messages):**
id - unique message number
message_date - date of the message
user_id - the identifier of the user who sent the message

**Internet table (information about internet sessions):**
id - unique session number
mb_used - the amount of Internet traffic spent per session (in megabytes)
session_date - date of the internet session
user_id - user ID

**Table tariffs (information on tariffs):**
tariff_name - tariff name
rub_monthly_fee - monthly subscription fee in rubles
minutes_included - the number of minutes of conversation per month included in the subscription fee
messages_included - number of messages per month included in the subscription fee
mb_per_month_included - the amount of Internet traffic included in the subscription fee (in megabytes)
rub_per_minute - the cost of a minute of conversation in excess of the tariff package (for example, if the tariff has 100 minutes of conversation per month, then a fee will be charged from 101 minutes)
rub_per_message - the cost of sending a message in excess of the tariff package
rub_per_gb - the cost of an additional gigabyte of Internet traffic in excess of the tariff package (1 gigabyte = 1024 megabytes)

*Action plan:*
1. Exploring general information about the data file
2. Data preprocessing
3. Exploratory data-driven analysis
4. Statistical analysis and hypothesis testing
5. General conclusion
