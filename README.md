# Аналитический отчет о проделанной работе по дисциплине "Эконометрика"
## Команда №9
Федоров Дмитрий Андреевич - БЭК194 \
Дасмаева Мария Владимировна - БЭК197 \
Клечикова Маргарита Александровна - БЭК196 \
Рахманова Амина Фаридовна - БЭК196 \
Жигульская Евгения Леонидовна - БЭК193 \
Струговец Мария - БЭК195 \
Бухановская Юлия Алексеевна - БЭК197 

## Оглавление
1. [Описание](#first)

## <a name="first"> 1. Вводная часть, описывающая постановку и обоснование вопроса </a>
### 1.1 Постановка вопроса
Существует ли зависимость между экономическим состоянием штата США и количеством насильственных преступлений в нем?
### 1.2 Постановка гипотезы
Чем хуже экономические условия в штате, тем больше в нем происходит насильственных преступлений.
### 1.3 Теоретическая часть
Violent Crimes – насильственные преступления, которые включают: убийство, нападение, непредумышленное убийство, сексуальное насилие, ограбление, угроза, похищение, вымогательство и преследование. 

По общим показателям Америка относится к безопасной стране с высоким уровнем жизни и доходов.  

Тем не менее уровень преступности в США сильно отличается по штатам. Преступность является локальным явлением, и в некоторых штатах уровень насильственных преступлений все еще высок или выше, чем в начале 1990-х годов, сообщает [USA Today](https://www.usatoday.com/story/money/2020/01/13/most-dangerous-states-in-america-violent-crime-murder-rate/40968963/) на основе данных [Программы ФБР по отчетности о преступлениях в 2018 году](https://ucr.fbi.gov/crime-in-the-u.s/2018/crime-in-the-u.s.-2018/topic-pages/violent-crime).  

С точки зрения [криминологии](http://lib.maupfib.kg/wp-content/uploads/Kriminologiya_Pod-red-Dolgovoy-A.I_Uchebnik_2005-3-e-izd-912s.pdf), условие преступности — это то, что само по себе не порождает преступность или преступление, но влияет на процессы порождения, участвует в детерминации преступности. Так, условиями преступности могут являться обстоятельства, относящиеся к состоянию внешней среды, в том числе и экономическое состояние населенного пункта, где совершено преступление.  

Мы также должны упомянуть, что лучшее понимание и количественная оценка характера и масштабов преступности в Соединенных Штатах возможны только при тщательном изучении и анализе различных уникальных условий, влияющих на каждую местную правоохранительную юрисдикцию. Некоторые факторы, которые влияют на объем и тип преступлений, помимо экономических условий:  
+ Плотность населения и степень урбанизации
+ Различия в составе населения, особенно концентрация молодежи
+ Стабильность населения в отношении мобильности жителей, схемы поездок на работу и обратно, а также временных факторов
+ Виды передвижения и система автомобильных дорог
+ Культурные факторы и образовательные, рекреационные и религиозные характеристики
+ Семейные условия в отношении развода и сплоченности семьи
+ Климат
+ Эффективная сила правоохранительных органов
+ Административные и следственные акценты правоохранительных органов
+ Политика других компонентов системы уголовного правосудия (например, прокурорской, судебной, исправительной и условной)
+ Отношение граждан к преступности
+ Практика информирования граждан о преступлениях.  

Многие из этих факторов все равно так или иначе связаны с экономическими условиями в штате, так как уровень экономического развития штата так или иначе влияет на социальные условия в нем. Так как экономика — это система жизнеобеспечения людей и общества и по своей целевой направленности все экономические процессы в той или иной степени влияют на социальную сферу общества.  

Мы предполагаем, что уровень экономики в штатах США напрямую воздействует на уровень преступности. Так, штаты с ограниченными экономическими возможностями и значительным процентом жителей, испытывающих финансовые трудности, как правило, имеют более высокие уровни насильственных преступлений.  

Чтобы говорить об экономике в целом, мы выделили основные показатели, такие как доход, ВВП, уровни безработицы и бедности.  

Также можно сделать теоретические предположения, как эти показатели влияют на основную характеристику. Недостаточный уровень дохода является побудительным фактором для таких преступлений как ограбление и вымогательство, которые в свою очередь могут быть причиной нападения и даже убийства. Если говорить об уровне бедности, то люди за чертой бедности предположительно используют более жесткие методы обогащения, так как им нужно не просто найти дополнительный «заработок», а в целом найти средства существования, в таком случае можно говорить о преднамеренных убийствах ради наживы. Это лишь малейшая часть конкретных предположений, которые относятся далеко не ко всем преступлениям. Чтобы подробно изучить зависимость факторов в целом, мы будем исследовать данные за несколько лет в разных штатах, проверив таким образом нашу гипотезу.  
### 1.4 Актуальность вопроса
Нам кажется, что данный вопрос особенно актуален в современной Америке - страна пребывает в состоянии роста насильственной преступности. Тому подтверждение статья Guardian о небывалом росте убийств:  
> As a country, as a society, we don’t have a great answer to that, but we need to be trying, and innovating, and we need to be taking it [the problem of rising violence] seriously.  
>
Помимо этого, рост насильственной преступности - одна из важнейших политических тем, составляющая дебатов Республиканцев и Демократов, причина различных митингов. Нам кажется, что опыт подобного исследования может содействовать снижению роста преступности и повышению осведомленности о наиболее вероятных признаках надвигающейся угрозы. 

Наше исследование актуально, потому что оно покажет зависимость экономических условий штата и уровня преступности, что в свою очередь позволит сделать вывод о важности экономического роста и преодолении безработицы при борьбе с преступностью. 
## 2. Описание данных, разведанализ данных
### 2.1 Описание переменных
+ Vcrime - количество совершенных насильственных преступлений на 100 тысяч населения. 
+ PIPC - personal income per capita, all states. 
+ RGDP - real GDP, all industry, all states. 
+ UR - unemployment rate, all states. 
+ PR - poverty rate, according to Poverty Level. 
### 2.3 Разведанализ данных
В нашем исследовании мы используем данные по 50 штатам США с 2010 по 2019 год.
Чтобы изучить экономические условия штата, мы включили такие характеристики как количество
совершенных насильственных преступлений, уровень бедности и безработицы, а также доход и
реальный ВВП.

Данные были собраны с разных ресурсов, так что требуют некоторых преобразований для дальнейшего
анализа. \
Data \
Ссылка на [rmd-файл](https://github.com/zhiguslakaievg/Econometrics-Project/blob/main/%D1%80%D0%B0%D0%B7%D0%B2%D0%B5%D0%B4%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7.Rmd)
#### Рассмотрим обощающие данные по всем переменным:  
#### Переменная Year. 
Показывает год, за который были совершены преступления, является числовой.  

Мы взяли данные за 2010-2019 года, за 2020 не брали в целом, так как некоторые из необходимых значений будут известны лишь к концу 2021 - началу 2022 года из-за особенностей сбора статистики в отдельных штатах.  
#### Переменная State. 
State Description \
Текстовая переменная, обозначающая название штата. \
State Unique \
Имеет 50 уникальных значений.  
#### Переменная Vcrime. 
![Crimes Description](/Database/Images/crimes_desc.png)\
Числовая переменная, указывающий количество совершенных насильственных преступлений (violent crimes) на 100 тысяч населения. 

Значения колеблются в диапазоне от 112 до 885, где среднее (362) и медианное (339) близки друг к другу.  \
Crimes \
На графике видно, что количество регистрируемых наблюдений в целом находится на достаточно высоком уровне, что еще раз подтверждает выводы СМИ о существующей проблеме с насильственными преступлениями на территории Соединенных Штатов Америки. Статистический службы также зафиксировали и несколько экстремально высоких значений за все время наблюдения (почти 1000 преступлений). Подобные выбросы можно объяснить снижением затрат на финансирование правоохранительных органов, усилением расслоения общества, экономическими шоками. Следует заметить, что это могло произойти и вследствие ошибок при фиксации и регистрации насильственных преступлений.  
#### Переменная PR. 
![Poverty Rate Description](/Database/Images/pr_desc.png)\
Poverty rate - числовая переменная, означающая уровень бедности в долях, то есть от 0 до 1.  

В нашем случае минимальное значение 0.069, а максимальное 0.244. \
Poverty Rate \
Средний зафиксированный за весь период наблюдения уровень бедности по всем штатам показывает неплохие - относительно мировых - значения. По графику можно заметить, что уровень бедности падает с каждым годом, что несомненно служит хорошим показателем экономической эффективности штата. Тем не менее, стоит упомянуть и крайне высокие значения, близкие к 0,25. Эти показатели были зафиксированы в начале десятых годов (2012 и 2013). Сложно однозначно сказать, что послужило причиной подобных выбросов.  
#### Переменная UR.
![Unemployment Rate Description](/Database/Images/ur_desc.png)\
Unemployment rate - уровень безработицы в штатах в долях. Значения колеблются от 2,2% до 13,7%. \
Unemployment Rate \
На графике видно, что среднее значение и медиана колеблются около 5% уровня безработицы, как было в таблице. Кроме того, можно заметить, что показателей выше 11% довольно мало, по сравнению с остальными.  

Также видно, что в среднем в Соединенных Штатах Америки сохраняется достаточно низкий уровень безработицы, что может указывать на эффективность работы служб занятости и наличии свободных рабочих мест. Выбросы на графике можно объяснить локальными коллапсами или, например, длительным восстановлением после кризиса 2007-2009 годов. 
#### Переменная PIPC. 
![Personal income per capita Description](/Database/Images/pipc_desc.png)\
Personal income per capita - числовое значение, выражающее доход на душу населения в долларах. 

Максимальное значение (75794) более чем в два раза больше минимального (31284), хотя среднее и медианное значения чуть больше 45000. Получается, что значений, близких к максимальному, довольно мало. \
Personal income per capita \
Выбросы на графике можно объяснить спецификой данного показателя: он фиксирует все доходы человека (зарплата, доходы от аренды, дивиденды, трансферты и другие виды). Это приводит к следующей ситуации: в маленьких штатах показатель PIPC может быть либо слишком высоким, либо слишком низким из-за небывалой урожайности (особенно актуально для аграрно-зависимых штатов), природной катастрофы или крупного экономического проекта. В то же время дополнительное население (например, студенты колледжей из других штатов) может занижать показатели PIPC.  
#### Переменная RGDP.
![Real GDP Description](/Database/Images/rgdp_desc.png)\
Real GDP - числовое значение реального ВВП штата. За 10 лет он колеблется от 28404 до 2739343. \
Real GDP \
По графику видно, что некоторые значения сильно выбиваются по значению ВВП в большую сторону.  

Чтобы понять, как именно выглядит выброс, рассмотрим часть графика ближе: \
Real GDP Distribution \
Таким образом мы видим, что выбивается в большей степени штат Калифорнии.  

Посмотрим данные дополнительно:  \
California Data Description \
Таким образом мы видим, что штат Калифорния отличается от других штатов тем, что реальный ВВП с 2010 по 2019 год было выше 2000000, а у остальных штатов значительно ниже. Нельзя назвать это выбросом данных, так как все значения принадлежат одному штату за все года, то есть это реально
возможные значения.  

Нетрудно объяснить подобное отклонение реального ВВП: Калифорния - крупнейшая экономика в рамках Соединенных Штатов Америки, пятая по показателям ВВП даже среди стран. Одними из драйверов подобного успеха являются численность населения и диверсификация экономики(финансовый сектор и недвижимость, информационная отрасль, производственный сектор вносят наибольший вклад).  
### Общий вывод разведанализа. 
Нам удалось собрать достаточно большой датасет с данными за обширный период времени, на основе которого мы сможем проверить нашу гипотезу о наличии зависимости между экономическими условиями штата и количеством насильственных преступлений в нем. В рамках разведанализа нам удалось провести чистку данных и убедиться в правильности выбора переменных в рамках нашего исследования.  
## Формулировка и обоснование модели 
## Ожидаемые результаты
## Результаты регрессионного анализа
## Анализ результатов
## Ответ на содержательный вопрос в рамках проведенного анализа
## Критический анализ результатов и анализ ограничений исследования
## Предложения по возможному расширению исследования
## Заключение
## Вклад членов команды в групповую работу
|  	| Федоров  Д.А. 	| Дасмаева М.В. 	| Клечикова М.А. 	| Рахманова А.Ф. 	| Жигульская Е.Л. 	| Струговец М. 	| Бухановская Ю.А. 	|
|:---:	|:---:	|:---:	|:---:	|:---:	|:---:	|:---:	|:---:	|
| Оценка 1 	|  ---|  	|  	|  	|  	|  	|  	|
| Оценка 2 	|  	| --- 	|  	|  	|  	|  	|  	|
| Оценка 3 	|  	|  	| --- 	|  	|  	|  	|  	|
| Оценка 4 	|  	|  	|  	| --- 	|  	|  	|  	|
| Оценка 5 	|  	|  	|  	|  	| --- 	|  	|  	|
| Оценка 6 	|  	|  	|  	|  	|  	| --- 	|  	|
| Оценка 7 	|  	|  	|  	|  	|  	|  	| --- 	|
## Приложения с техническими результатами
## Приложения с кодами
## Источники
1. United Health Foundation, National Violent Crime Data. America’s Health Rankings. Retrieved from https://www.americashealthrankings.org/explore/annual/measure/Crime/state/ALL?edition-year=2020 
2. Local Area Unemployment Statistics. U.S. Bureau of Labor Statistics. Retrieved from https://www.bls.gov/lau/ 
3. Economic Data, Per Capita Personal Income, Real GDP. FRED. Retrieved from https://fred.stlouisfed.org/ 
4. Distribution of Total Population by Federal Poverty Level. KFF. Retrieved from https://www.kff.org/state-category/demographics-and-the-economy/people-in-poverty/ 
## Онлайн-приложения
1. [Основной датасет](/project_data.csv)
2. [База данных с исходниками](/Database) 
