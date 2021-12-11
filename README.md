# Аналитический отчет о проделанной работе по дисциплине "Эконометрика"
## Команда №9
Федоров Дмитрий Андреевич - БЭК194 \
Дасмаева Мария Владимировна - БЭК197 \
Рахманова Амина Фаридовна - БЭК196 \
Бухановская Юлия Алексеевна - БЭК197 \
Жигульская Евгения Леонидовна - БЭК193 \
Клечикова Маргарита Александровна - БЭК196 \
Струговец Мария - БЭК195

## Оглавление
1. [Вводная часть](#one) \
  1.1 [Постановка вопроса](#oneone) \
  1.2 [Постановка гипотезы](#onetwo) \
  1.3 [Теоретическая часть](#onethree) \
  1.4 [Актуальность вопроса](#onefour) 
2. [Описание и разведанализ данных](#two) \
  2.1 [Описание данных](#twoone) \
  2.2 [Разведанализ данных](#twotwo)\
      2.2.1 [Анализ переменных](#twotwoone) \
      2.2.2 [Корреляция между переменными](#twotwotwo) \
      2.2.3 [Парные регрессии](#twotwothree) \
      2.2.4 [Проверка данных на гетероскедастичность](#twotwofour) \
      2.2.5 [Общий вывод](#twotwofive)
3. [Формулировка и обоснование модели](#three)
4. [Ожидаемые результаты](#four)
5. [Результаты регрессионного анализа](#five)
6. [Анализ результатов](#six)
7. [Ответ на содержательный вопрос](#seven)
8. [Критический анализ результатов и анализ ограничений исследования](#eight)
9. [Предложения по возможному расширению исследования](#nine)
10. [Заключение](#ten)
11. [Вклад членов команды](#eleven)
12. [Приложения с техническими результатами](#twelve)
13. [Приложения с кодами](#thirteen)
14. [Источники](#fourteen)
15. [Онлайн-приложения](#fifteen)

## <a name="one"> 1. Вводная часть, описывающая постановку и обоснование вопроса </a>
### <a name="oneone"> 1.1 Постановка вопроса </a>
Существует ли зависимость между экономическим состоянием штата США и количеством насильственных преступлений в нем?

### <a name="onetwo"> 1.2 Постановка гипотезы </a>
При прочих равных уровень насильственных преступлений в штате не зависит от экономических условий.

### <a name="onethree"> 1.3 Теоретическая часть </a>
Статистические данные о конкретных преступлениях индексируются в ежегодных [Единообразных отчетах](https://www.fbi.gov/services/cjis/ucr) о преступлениях Федерального бюро расследований (ФБР) и в ежегодных Национальных обзорах виктимизации преступлений, проводимых [Бюро статистики юстиции](https://bjs.ojp.gov/). В дополнение к основному Единому отчету о преступлениях, известному как *Преступность в Соединенных Штатах*, ФБР публикует ежегодные отчеты о состоянии правоохранительных органов в Соединенных Штатах. Содержащиеся в докладе определения конкретных преступлений считаются стандартными многими американскими правоохранительными органами. По данным ФБР, индекс преступности в Соединенные Штаты входят насильственные преступления и имущественные преступления. 

Violent Crimes – насильственные преступления, которые включают: убийство, нападение, непредумышленное убийство, сексуальное насилие, ограбление, угроза, похищение, вымогательство и преследование. 

По общим показателям Америка относится к безопасной стране с высоким уровнем жизни и доходов.  

Тем не менее уровень преступности в США сильно отличается по штатам. Преступность является локальным явлением, и в некоторых штатах уровень насильственных преступлений все еще высок или выше, чем в начале 1990-х годов, сообщает [USA Today](https://www.usatoday.com/story/money/2020/01/13/most-dangerous-states-in-america-violent-crime-murder-rate/40968963/) на основе данных [Программы ФБР по отчетности о преступлениях в 2018 году](https://ucr.fbi.gov/crime-in-the-u.s/2018/crime-in-the-u.s.-2018/topic-pages/violent-crime). 

В 2019 году, [по данным ФБР](https://ucr.fbi.gov/crime-in-the-u.s/2019/crime-in-the-u.s.-2019/topic-pages/cius-summary), в Соединенных Штатах произошло примерно 1 203 808 насильственных преступлений. На 100 000 человек, проживающих в Соединенных Штатах, было произведено 156 арестов, в той или иной степени связанных с насильственными преступлениями. Более конкретно, на каждые 100 000 человек было произведено 3 ареста за убийство, 7 за изнасилование, 24 за грабеж, а нападение было наиболее распространенным: на каждые 100 000 человек было произведено 120 арестов.

С точки зрения [криминологии](http://lib.maupfib.kg/wp-content/uploads/Kriminologiya_Pod-red-Dolgovoy-A.I_Uchebnik_2005-3-e-izd-912s.pdf), условие преступности — это то, что само по себе не порождает преступность или преступление, но влияет на процессы порождения, участвует в детерминации преступности. Так, условиями преступности могут являться обстоятельства, относящиеся к состоянию внешней среды, в том числе и экономическое состояние населенного пункта, где совершено преступление.  

Мы также должны упомянуть, что лучшее понимание и количественная оценка характера и масштабов преступности в Соединенных Штатах возможны только при тщательном изучении и анализе различных уникальных условий, влияющих на каждую местную правоохранительную юрисдикцию. Некоторые факторы, которые влияют на объем и тип преступлений, [по данным ФБР](https://ucr.fbi.gov/hate-crime/2011/resources/variables-affecting-crime), помимо **экономических условий**:  

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

Мы предполагаем, что уровень экономики в штатах США напрямую воздействует на уровень преступности. Так, штаты с ограниченными экономическими возможностями и значительным процентом жителей, испытывающих финансовые трудности, как правило, имеют более высокие уровни насильственных преступлений, согласно статье [USA Today](https://www.usatoday.com/story/money/2020/01/13/most-dangerous-states-in-america-violent-crime-murder-rate/40968963/).

Чтобы говорить об экономике в целом, мы выделили основные показатели, такие как: **доход, ВВП, уровни безработицы и бедности**.  

Также можно сделать теоретические предположения, как эти показатели влияют на основную характеристику. Недостаточный уровень дохода является побудительным фактором для таких преступлений как ограбление и вымогательство, которые в свою очередь могут быть причиной нападения и даже убийства. Если говорить об уровне бедности, то люди за чертой бедности предположительно используют более жесткие методы обогащения, так как им нужно не просто найти дополнительный «заработок», а в целом найти средства существования, в таком случае можно говорить о преднамеренных убийствах ради наживы. Это лишь малейшая часть конкретных предположений, которые относятся далеко не ко всем преступлениям. Чтобы подробно изучить зависимость факторов в целом, мы будем исследовать данные за несколько лет в разных штатах, проверив таким образом нашу гипотезу.  

### <a name="onefour"> 1.4 Актуальность вопроса </a>
Нам кажется, что данный вопрос особенно актуален в современной Америке - страна пребывает в состоянии роста насильственной преступности. Тому подтверждение [статья Guardian о небывалом росте убийств](https://www.theguardian.com/us-news/2021/sep/27/us-murder-rate-increase-2020):  
> As a country, as a society, we don’t have a great answer to that, but we need to be trying, and innovating, and we need to be taking it [the problem of rising violence] seriously.  
>
Помимо этого, рост насильственной преступности - одна из важнейших политических тем, составляющая дебатов Республиканцев и Демократов, причина различных митингов. Нам кажется, что опыт подобного исследования может содействовать снижению роста преступности и повышению осведомленности о наиболее вероятных признаках надвигающейся угрозы.

О влиянии преступности на социально-экономическое развитие страны говорится в статье [“Impacts of Crime on Socio-Economic Development”](https://www.researchgate.net/publication/354382389_Impacts_of_Crime_on_Socio-Economic_Development). Преступность часто является препятствием на пути социально-экономического роста общества, препятствует инвестициям, увеличивает стоимость транзакций и, в конечном итоге, способствует миграции, которая в конечном итоге создает диспропорции в экономическом развитии во всем мире.

Наше исследование актуально, потому что оно покажет зависимость экономических условий штата и уровня преступности, что в свою очередь позволит сделать вывод о важности экономического роста и преодолении безработицы при борьбе с преступностью. 

## <a name="two"> 2. Описание данных, разведанализ данных </a>
### <a name="twoone"> 2.1 Описание переменных </a>

| Тип переменной | Название переменной | Описание переменной |
|:---:|:---:|:---:|
| Зависимая | Vcrime | Количество совершенных насильственных преступлений <br>на 100 тысяч населения |
| Переменная<br>Интереса | PIPC | Доход на душу населения, $ |
| Переменная<br>Интереса | RGDP | Реальный ВВП, $ |
| Переменная<br>Интереса | UR | Уровень безработицы, доли |
| Переменная<br>Интереса | PR | Уровень бедности, доли |
| Контрольная | Density | Плотность населения, миля^2  |
| Контрольная | Marriage | Количество браков на 1000 населения |
| Контрольная | Divorce | Количество разводов на 1000 населения |
| Контрольная | Immigrants | Количество иммигрантов, которые получили законное постоянное место жительства, находятся в США на временной основе, подали заявление о предоставлении убежища или статуса беженца или были натурализованы |
| Контрольная | Temperature | Средняя температура, F |

### <a name="twotwo"> 2.2 Разведанализ данных </a>

**Полный разведанализ** можно прочитать здесь: [pdf файл](Database/PDF/data_analysis_final.pdf)\
**Код разведанализа** можно найти здесь: [Rmd файл](Database/RMD/data_analysis_final.Rmd)

В нашем исследовании мы используем **усредненные за период с 2010 по 2019 данные по 50 штатам США**

#### Почему мы усреднили данные? 

Чтобы исключить зависимость значений одного и того же штата в разные года, нам нужно было усреднить данные или выбрать кросс-секцию. Мы приняли решение усреднить значения за 10 лет, так как, по нашему мнению, это более объективно отражает ситуацию с уровнем преступности и экономическими условиями. Данные за какой-то конкретный год более подвержены влиянию внешних факторов и могут быть смещены, в данном случае средние показатели помогут нам избежать этого.

Чтобы изучить экономические условия штата, мы включили такие характеристики, как количество совершенных насильственных преступлений, уровень бедности и безработицы, а также доход и реальный ВВП. Кроме того, мы добавили несколько контрольных переменных: плотность населения, число иммигрантов в штате, количество браков и разводов а также среднюю температуру в штате.

[Предварительный просмотр данных.](Database/CSV/project_data_full.csv) 

### <a name="twotwoone">Рассмотрим переменные более подробно:</a>  

[Файл с описательной статистикой в CSV](Database/CSV/describe.csv)

<a name="describe">Таблица с описательной статистикой:</a>

|  | min | max | mean | median | sd | Q0.25 | Q0.75 |
|---|---|---|---|---|---|---|---|
| [Vcrime](#vcrime)| 121.74 | 702.87 | 362.85 | 336.98 | 137.11 | 261.1 | 460.54 |
| [PR](#pr) | 0.08 | 0.22 | 0.14 | 0.14 | 0.03 | 0.11 | 0.16 |
| [UR](#ur) | 0.03 | 0.08 | 0.06 | 0.06 | 0.01 | 0.05 | 0.07 |
| [PIPC](#pipc) | 35163.3 | 67553.1 | 46784.62 | 45520.95 | 7101.26 | 41759.12 | 50863.9 |
| [RGDP](#rgdp) | 29179.94 | 2335825.91 | 339150.52 | 191782.82 | 423849.7 | 78560.87 | 442790.42 |
| [Density](#density) | 1.25 | 1229.25 | 200.73 | 105.15 | 267.97 | 45.76 | 217.05 |
| [Immigrants](#immi) | 449.9 | 204678.6 | 21081 | 6432 | 38931.9 | 3124.7 | 18599.35 |
| [Marriage](#mar) | 5.26 | 31.5 | 7.36 | 6.63 | 3.85 | 6.07 | 7.21 |
| [Divorce](#div) | 6.15 | 12.25 | 9.06 | 9.1 | 1.53 | 7.82 | 10.09 |
| [Temperature](#temp) | 29.06 | 71.93 | 52.98 | 52.4 | 8.76 | 46.52 | 59.35 |

#### Переменная State. 

Текстовая переменная, обозначающая название штата, имеющая [50 уникальных значений](Database/Images/state_unique.png)

#### Переменная <a name="vcrime">Vcrime</a> 

Числовая переменная, указывающий количество совершенных насильственных преступлений (violent crimes) на 100 тысяч населения. Значения [колеблются](#describe) в диапазоне от 122 до 703, где [среднее](#describe) (363) и [медианное](#describe) (337) близки друг к другу.

Мы построили [график](Database/Images/crimes.png), который показывает количество наблюдений и их плотность в стране. Таким образом выяснили, что количество регистрируемых наблюдений в целом находится на достаточно высоком уровне, что еще раз подтверждает выводы СМИ о существующей проблеме с насильственными преступлениями на территории Соединенных Штатов Америки.

#### Переменная <a name="pr">PR</a>

Poverty rate - числовая переменная, обозначающая уровень бедности в долях, то есть от 0 до 1. В нашем случае [минимальное значение](#describe) 0.0818, а [максимальное](#describe) 0.2173.

Этот тренд мы можем заметить и на [графике рассеивания](Database/Images/dispPR.png).

Почти все штаты показывают неплохие - относительно мировых - результаты по уровню бедности. Тем не менее, есть штаты, которые за десять лет наблюдений все так же имеют достаточно высокую (близко к 0.2 и выше) долю населения, находящегося за чертой бедности. Это может объясняться локальными экономическими, географическими и климатическими особенностями, которые мешают развитию штата.

#### Переменная <a name="ur">UR</a>

Unemployment rate - уровень безработицы в штатах в долях. Значения [колеблются](#describe) от 2,9% до 8,3%. 

На графике вида [scatter plot](Database/Images/dispUR.png) действительно можно наблюдать некоторую зависимость. 

Следует также заметить, что уровень безработицы в США в среднем держится на оптимальном уровне, потому что падения ниже 5%, как правило, приводят к снижению общего уровня выпуска и усилению инфляции. Подобные значения также говорят об эффективности работы Федеральной Резервной Системы.

#### Переменная <a name="pipc">PIPC</a> 

Personal income per capita - числовое значение, выражающее доход на душу населения в долларах. [Максимальное значение](#describe) (67553) более чем в два раза больше [минимального](#describe) (35163), хотя [среднее и медианное](#describe) значения чуть больше 45000. Таким образом значений, близких к максимальному, довольно мало. 

Рассмотрим [график](Database/Images/boxplotPIPC.png) типа boxplot.

Уровень дохода приходится в основном на промежуток от 43 до 51 тысячи долларов на душу населения. Это позволяет сделать вывод о томб что доходы жителей большинства штатов находятся именно в этом отрезке.

Тем не менее, присутствуют значение, которое выделяется из массы остальных. Проверим штаты с уровнем дохода выше 60000:

|  | State | PIPC |
|---|---|---|
| 1 | Connecticut | 67553.1 |
| 2 | Massachusetts | 62083.9 |

Выбросы в данных - зачение уровня дохода в двух штатах. Большую долю в экономике Коннектикута составляет доход от военно-промышленных корпораций, так как это главный арсенал страны, а также страховой бизнес - один из наиболее популярных в штате. Массачусетс - один из мировых центров биотехнологий, искусственного интеллекта и венчурного капитала.

Выбросы можно объяснить спецификой данного показателя: он фиксирует все доходы человека (зарплата, доходы от аренды, дивиденды, трансферты и другие виды). Однако в данном случае это может влиять на корреляцию между переменными, так что попробуем прологарифмировать значение PIPC. Логарифм делает показатели относительными, что позволяет избавиться от [выбросов](Database/Images/boxplotlogPIPC.png). 

В рамках показателя Personal Income per Capita наблюдается положительная тенденция: усреднённые за 10 лет данные показывают, что доход на душу населения находится на достаточно высоком уровне почти во все штатах, что свидетельствует о приемлемом состоянии экономики. Кроме того, следует отметить, что подобные показатели достигаются, в том числе, благодаря западной контрактной системе с фиксированными почасовыми ставками.

#### Переменная <a name="rgdp">RGDP</a>

Real GDP - числовое значение реального ВВП штата. За 10 лет он [колеблется](#describe) от 29180 до 2335826. 

[Максимальное значение](#describe) = 2335826, а значение [3-го квартиля](#describe) = 442790. Это говорит об очень сильных выбросах. Посмотрим график типа [boxplot](Database/Images/boxplotRGDP.png)

На нем видны выбросы в виде трех штатов. Проверим значения выше 700000: 

|  | State | RGDP |
|---|---|---|
| 1 | California | 2335825.91 |
| 2 | Texas | 1550373.9 |
| 3 | New York | 1371720.34 |
| 4 | Florida | 849951.18 |
| 5 | Illinois | 741158.3 |

Действительно, мы видим, что 3 штата - Калифорния, Техас и Нью-Йорк - отличаются от других тем, что реальный ВВП с 2010 по 2019 был выше 1300000, а у остальных штатов значительно ниже. В рамках [полного разведанализа](Database/PDF/data_analysis_final.pdf) мы убедились, что объяснить подобное отклонение реального ВВП нетрудно.

Однако эти выбросы могут отрицательно повлиять на наши будущие оценки, поэтому [логарифмируем](Database/Images/boxplotlogRGDP.png) переменную.

В рамках показателя Real GDP наблюдается тенденция к росту показателя в зависимости от размера и численности населения штата, его ранга бизнес-среды, скопления высокотехнологичных производств и размерности рынка венчурного капитала.

#### Переменная <a name="density">Density</a>

Density - плотность насселения на единицу плозади в квадратных милях.

Разброс данных [велик](#describe): от 1.25 до 1229.25. При этом третий квантиль [составляет](#describe) всего 217.05, скорее всего присутствуют некие выбросы. Проверим значения в два раза больше границы квантиля.

|  | State | Density |
|---|---|---|
| 1 | New Jersey | 1229.25 |
| 2 | Rhode Island | 1039.75 |
| 3 | Massachusetts | 870.3 |
| 4 | Connecticut | 741.4 |
| 5 | Maryland | 615.45 |

Мы видим 5 штатов с высоким уровнем плотности. Несложно объяснить подобные выбросы: представленные в списке штаты являются одними из самых маленьких по площади в США, но не самыми малочисленными по населению.

Данные нарастают относительно пропорционально и имеют логические объяснения, поэтому оставим их в изначальном виде.

#### Переменная <a name="immi">Immigrants</a>

Immigrants - количество иммигрантов, которые получили законное постоянное место жительства, находятся в США на временной основе, подали заявление о предоставлении убежища или статуса беженца или были натурализованы.

Снова сталкиваемся с проблемой разброса данных: [максимальное значение](#describe) в 10 раз больше среднего. Оценим значения, большие хотя бы в 2 раза.

|  | State | Immigrants |
|---|---|---|
| 1 | California | 204678.6 |
| 2 | New York | 140910.4 |
| 3 | Florida | 116317.5 |
| 4 | Texas | 99873.1 |
| 5 | New Jersey | 53156.2 |

Выделяются 5 довольно крупных и популярных штата. Объяснить выбросы в количестве иммигрантов не составляет трудностей: большая часть представленных в списке штатов являются наиболее развитыми и привлекательными для миграции из-за высокого уровня дохода и лучших условий жизни. Эти штаты являются домом для крупнейших стартапов, имеют лучшую систему образования и идеальные карьерные перспективы.

Данные выбросы объяснимы и логичны, поэтому оставим их в изначальном виде.

#### Переменная <a name="mar">Marriage</a>

Marriage - количество браков на 1000 человек.

При [максимальном значении](#describe) 31,5 граница третьего квантиля находится на [довольно низком уровне](#describe) (7,21), возможны выбросы. Проверим значения, выбивающиеся более чем в два раза:

|  | State | Marriage |
|---|---|---|
| 1 | Nevada | 31.502662549274 |
| 2 | Hawaii | 16.2975960934697 |

Невада и Гавайи уже длительное время являются лидерами по количеству браков. Несложно объяснить подобные выбросы: Лас-Вегас (штат Невада) славится самым простым законодательством по отношению к заключению брака - это штат "быстрых" браков. Гавайи появились в этом списке неслучайно: штат является экзотическим направлением для многих пар, желающих заключить брак в необычных условиях и при различных сюжетах на любой бюджет.

Оставим данные в исходном формате.

#### Переменная <a name="div">Divorce</a>

Divorce - количество разводов на 1000 человек.

Нет никаких выбросов или [отличительных свойств](#describe). Данные предположительно нормально распределены, что не мешает в дальнейшей модели.

#### Переменная <a name="temp">Temperature</a>

Temperature - средняя температура в штате по Фаренгейту. Чтобы было легче воспринимать, на этапе анализа мы переведем данные в градусы по Цельсию.

В целом, [можно заметить](#describe), что никаких выбросов нет и значения более или менее нормально распределены, поэтому оставляем их в изначальном виде - в градусах по Фаренгейту.

### <a name="twotwotwo">Корреляция между переменными </a>

Для подробного анализа мы также проверили корреляцию между зависимой переменной Vcrime и объясняющими и контрольными переменными.

С результатами можно ознакомиться в [соответствующем файле](Database/PDF/analysis_correlation.pdf)

|  | Vcrime | PR | UR | PIPC | RGDP | logPIPC |
|---|---|---|---|---|---|---|
| PR | 0.41702 |  |  |  |  |  |
| UR | 0.46002 | 0.51298 |  |  |  |  |
| PIPC | -0.17195 | -0.74873 | -0.19432 |  |  |  |
| RGDP | 0.14664 | 0.09647 | 0.33579 | 0.25378 |  |  |
| logPIPC | -0.17469 | -0.77363 | -0.22181 | 0.99609 | 0.26278 |  |
| logRGDP | 0.22073 | 0.13365 | 0.42050 | 0.17917 | 0.82532 | 0.18031 |

|  | RGDP | Density | Immigrants | Marriage | Divorce |
|---|---|---|---|---|---|
| Density | 0.19863 |  |  |  |  |
| Immigrants | 0.94780 | 0.25143 |  |  |  |
| Marriage | -0.14353 | -0.18209 | -0.08215 |  |  |
| Divorce | -0.25462 | -0.46456 | -0.26433 | 0.23890 |  |
| Temperature | 0.26231 | 0.11879 | 0.25057 | 0.07890 | 0.17616 |

Коэффициент, близкий или больший по модулю 0,5, означает высокую взаимосвязь между переменными. Ниже 0,5, соответственно, свидетельствует о слабой взаимосвязи.

На данной схеме мы можем увидеть, что существует довольно высокая корреляция переменной Vcrime с переменными PR (0,42) и UR (0,46). С переменными Temperature (0,31) и Divorce (0,29) прослеживается средняя корреляция. Остальные же довольно плохо коррелируют с числом насильственных преступлений. 

Также стоит заметить, что логарифмирование отдельных показателей не сильно улучшило ситуацию, хотя они и изменились немного в большую сторону. 

### <a name="twotwothree"> Парные регрессии </a>

Дополнительно построим парную регрессию между переменными для проверки взаимосвязи.

С результатами можно ознакомиться в [соответствующем файле](Database/PDF/analysis_regression.pdf)

Проверив t-test для каждой переменной отдельно, можно определить их значимость по значению p-value.

Таким образом, мы получили аналогичный предыдущему пункту результат, а именно: наиболее значимыми для анализа показателей Vcrime являются переменные PR и UR, при этом существует небольшая связь с переменными Temperature и Divorce

### <a name="twotwofour"> Проверка данных на гетероскедастичность </a>

Так как графики данных неоднозначны, а наши предположения затрагивают только некоторые переменные, стоит проверить их на наличие гетероскедастичности с помощью теста Бройша-Пагана, где p-value < 0,5 свидетельствует о гетероскедастичности данных (гипотеза о гомоскедастичности отвергается).

Ознакомиться с результатами проведенных тестов можно в [соответствующем файле](Database/PDF/analysis_heteroscedasticity.pdf)

Таким образом, показатели гетероскедастичны для переменных логарифма ВВП и температуры. Для сглаживания данного эффекта в итоговой модели будем считать робастные ошибки. 

### <a name="twotwofive"> Общий вывод </a>

Нам удалось собрать датасет с усредненными данными за обширный период времени, на основе которого мы сможем проверить нашу гипотезу о наличии зависимости между экономическими условиями штата и количеством насильственных преступлений в нем. В рамках разведанализа нам удалось провести необходимую чистку и изменение данных и убедиться в правильности выбора переменных в рамках нашего исследования

## <a name="three"> 3. Формулировка и обоснование модели </a>
Мы сформулировали модель следующим образом:

```
Vcrime = β0 + β1*PR + β2*UR + β3*logPIPC + β4*logRGDP
```
+ *Vcrime* - зависимая переменная; 

+ *PR (Poverty Rate), UR (Unemployment Rate), PIPC (Personal Income per Capita), RGDP (Real GDP)* - объясняющие переменные; 

+ *β0, β1, β2, β3, β4* - коэффициенты регрессии

**Обоснование модели**

Учитывая поставленный вопрос, мы решили выбрать именно эти переменные, поскольку они лучше всего отражают экономическое состояние отдельно взятого штата. **Poverty Rate** отлично отражает возможности рынка труда обеспечивать предложение рабочих мест. **Unemployment Rate** - один из важнейших индикаторов состояния экономики, который, помимо прочего, определяет монетарную политику государства. **Personal Income per Capita** позволяет определить стандарты жизни для населения отдельных географических регионов (в нашем случае - штатов). **Real GDP** показывает фактический рост производства без искажений от инфляции. Таким образом, совокупность выбранных переменных позволяет наиболее точно определить состояние экономики каждого штата, что и требуется в нашей гипотезе.

Кроме того, мы приняли решение прологарифмировать переменные PIPC и RGDP из-за наличия выбросов и большого разброса значений. А также из-за наличия гетероскедастичности в переменной RGDP мы рассчитали робастные оценки. 

*Подробный разбор причины и анализ переменных можно увидеть в разделе "Разведанализ данных".*

**Постановка гипотезы** 

**Содержательная постановка:** при прочих равных уровень насильственных преступлений в штате не зависит от экономических условий 

Для большей точности нашего исследования мы решили помимо одной гипотезы об общем экономическом состоянии штата проверить еще несколько о влиянии каждой переменной на уровень насильственных преступлений. Таким образом, у нас получается еще 4 гипотезы:
- При прочих равных уровень насильственных преступлений в штате не зависит от уровня бедности
- При прочих равных уровень насильственных преступлений в штате не зависит от уровня безработицы
- При прочих равных уровень насильственных преступлений в штате не зависит от дохода на душу населения
- При прочих равных уровень насильственных преступлений в штате не зависит от ВВП 

**Гипотеза в нормальной форме:** 
```
Ho: {β1 = 0;
     β2 = 0;
     β3 = 0;
     β4 = 0}

Ha: {Ho неверна}
```


## <a name="four"> 4. Ожидаемые результаты </a>

Мы предполагаем, что существует прямая зависимость между уровнем бедности и безработицы и количеством преступлений в штате. Также мы думаем, что чем ниже реальный ВВП и доход на душу населения в штате, тем чаще совершаются насильственные преступления в нем. Как итог, мы ожидаем получить результаты исследования, позволяющие утверждать, что зависимость между экономическим состоянием штата и уровнем насильственных преступлений в нем существует.

## <a name="five"> 5. Результаты регрессионного анализа </a>

[Полноценные результаты регрессионного анализа](/Database/PDF/regression.pdf)

|  | (1) | (2) | (3) | (4) | (5) |
|:---:|:---:|:---:|---|---|---|
| PR | 2,138.744**<br>(1,052.294) | 2,062.050*<br>(1,053.966) | 2,271.531**<br>(1,077.997) | 2,541.297**<br>(1,145.373) | 2,175.767*<br>(1,212.913) |
| UR | 3,213.337<br>(2,338.725) | 4,221.677*<br>(2,555.807) | 4,248.637*<br>(2,533.358) | 2,532.364<br>(2,678.679) | 3,389.587<br>(2,756.160) |
| log(PIPC) | 233.100<br>(171.319) | 337.188<br>(215.487) | 402.986*<br>(238.377) | 435.240*<br>(227.457) | 488.346**<br>(226.749) |
| log(RGDP) | -0.431<br>(24.742) | -0.236<br>(22.327) | 11.073<br>(25.110) | 24.067<br>(27.018) | 15.445<br>(28.618) |
| Density |  | -0.103<br>(0.099) | -0.109<br>(0.098) | -0.050<br>(0.096) | -0.094<br>(0.091) |
| Immigrants |  |  | -0.0005<br>(0.0005) | -0.001<br>(0.0004) | -0.001<br>(0.0004) |
| Marriage |  |  |  | 7.544**<br>(3.552) | 6.179<br>(3.833) |
| Divorce |  |  |  | 11.920<br>(15.024) | 9.954<br>(15.335) |
| Temperature |  |  |  |  | 2.277<br>(2.555) |
| Constant | -2,621.382<br>(1,790.169) | -3,768.536*<br>(2,272.633) | -4,632.517*<br>(2,603.459) | -5,250.774**<br>(2,498.331) | -5,797.038**<br>(2,468.757) |
| Note: |  |  | *p<0.1; | **p<0.05 | ***p<0.01 |

В первой модели (четыре изначально предполагаемые переменные) нулевая гипотеза отвергается только для PR.

Из-за появления контрольных переменных значимые переменные меняются. Однако значение уровня бедности (PR) значимо в любой модели. Также можно сказать, что логарифмируемый уровень дохода также значим при добавлении контрольных переменных.

Таким образом, нулевая гипотеза отвергается для экономического состояния в целом на любом уровне значимости.

Согласно нашей модели, на уровне значимости 5% значимыми являются следующие переменные:
* Уровень бедности
* Логарифм дохода на душу населения (является значимой на уровне значимости 1%)

Затем мы провели несколько тестов Вальда для проверки гипотезы, и они подтвердили наши результаты: **нулевая гипотеза отвергается только для переменных PR и PIPC.**

Также мы провели отдельный тест Вальда, чтобы проверить, значимы ли в целом наши переменные интереса. Согласно этому тесту, **экономический статус значим на уровне значимости 1%.**

## <a name="six"> 6. Анализ результатов </a>

В [результате нашего исследования](Database/PDF/regression.pdf) мы выяснили, что на количество насильственных преступлений в штате из всех факторов, исследуемых нами, влияние оказывают такие переменные, как уровень бедности (PR) и доход на душу населения (PIPC).

Мы предполагаем, что такой результат обосновывается тем, что бедность и низкий доход является сильнейшим детерминантом преступности. 
Прежде всего внутреннее состояние личности, внешне выраженное в бедности и низких доходах, негативно влияет на психологическое развитие и нравственные ориентиры. В связи с этим накапливаются обиды, неудовлетворенность становится обыденностью, что в дальнейшем приводит к противопоставлению себя социуму, девиантному поведению и желанию решить финансовые проблемы, прибегнув к совершению преступлений.

Что касается переменных не оказавших влияние на уровень преступности в штате: ситуация с безработицей в США в целом находится под контролем государства. Благодаря сильной социальной поддержке, безработные практически ни в чём не нуждаются. Даже минимально гарантированный уровень социальной помощи обеспечивает нормальную жизнь – без излишеств, но умеренно комфортную. В связи с этим мы можем утверждать, что отсутствие работы у индивида в США зачастую не означает его нужду в деньгах или наличие проблем в социальной сфере, что бы могло сподвигнуть его к совершению преступлений.

Такая переменная как реальный ВВП учитывает отражает рыночную стоимость товаров и услуг, произведенных в штате и отражает общую ситуации экономики в целом, а не отдельных индивидов. Анализируя данную переменную, сложно утверждать о наличии и количестве в штате лиц за чертой бедности, склонных к преступлениям.

## <a name="seven"> 7. Ответ на содержательный вопрос в рамках проведенного анализа </a>

В результате исследования мы выяснили, что существует зависимость между уровнем бедности и доходом на душу населения и количеством насильственных преступлений, в то же время такие переменные как реальный ВВП и уровень безработицы существенного влияния на количество насильственных преступлений не оказывают. Поскольку экономическое состояние штата описывается не одной переменной, а несколькими разными, мы отдельно проверили общее влияние этих переменных и имеем основания утверждать, что зависимость между ним (экономическим состоянием штата) и количеством насильственных преступлений существует. **Наша основная гипотеза подтвердилась.**

## <a name="eight"> 8. Критический анализ результатов и анализ ограничений исследования </a>

Можно лишь предположить, почему технически мы получили результат, отличный от наших предположений. Однако стоит учесть, что на данный момент мы ограничены определенным уровнем знаний, то есть можем провести конкретные тесты гипотез и корреляции данных. Кроме того, мы не могли использовать панельные данные, поэтому пришлось усреднять значения. Таким образом, технически результаты могут иметь некоторое отличие от более подробного анализа в других реалиях. На данный момент мы получили такой результат, что наши ожидания оправдались лишь на 25%, а точнее только одна значимая переменная из 4 желаемых.

## <a name="nine"> 9. Предложения по возможному расширению исследования </a>

## <a name="ten"> 10. Заключение </a>

## <a name="eleven"> 11. Вклад членов команды в групповую работу </a>
|                  	| Доля участия 	| Вклад в рамках проекта 	|
|:----------------:	|:------------:	|:----------------------:	|
| Федоров Д.А.     	|  25%        | Поиск данных, работа над разведанализом        |
| Дасмаева М.В.    	|  25%        | Создание моделей, работа над разведанализом                       	|
| Рахманова А.Ф.   	|  25%        | Создание моделей, работа над разведанализом                       	|
| Бухановская Ю.А.  |  15%          | Создание презентации, работа над результатами                      	|
| Жигульская Е.Л. 	|  10%          | Работа над разведанализом                       	|
| Клечикова М.А.    |  0%        |                        	|
| Струговец М.	    |  0%        |                        	|
| Итого             |  100%       	|                        	|

## <a name="twelve"> 12. Приложения с техническими результатами </a>

1. [Результаты регрессионного анализа и статистических тестов](Database/PDF/regression.pdf)
2. [Результаты анализа парной регрессии](Database/PDF/analysis_regression.pdf)
3. [Результаты анализа корреляции между переменными](Database/PDF/analysis_correlation.pdf)
4. [Результаты проверки данных на гетероскедастичность](Database/PDF/analysis_heteroscedasticity.pdf)

## <a name="thirteen"> 13. Приложения с кодами </a>

1. [Код разведанализа](Database/RMD/data_analysis_final.Rmd)
2. [Код для проведения регрессионного анализа и статистических тестов](Database/regression.rmd)

## <a name="fourteen"> 14. Источники </a>
1. United Health Foundation, National Violent Crime Data. America’s Health Rankings. Retrieved from https://www.americashealthrankings.org/explore/annual/measure/Crime/state/ALL?edition-year=2020 
2. Local Area Unemployment Statistics. U.S. Bureau of Labor Statistics. Retrieved from https://www.bls.gov/lau/ 
3. Economic Data, Per Capita Personal Income, Real GDP. FRED. Retrieved from https://fred.stlouisfed.org/ 
4. Distribution of Total Population by Federal Poverty Level. KFF. Retrieved from https://www.kff.org/state-category/demographics-and-the-economy/people-in-poverty/ 
5. The Uniform Crime Reporting (UCR) Program. FBI. Retrieved from (https://www.fbi.gov/services/cjis/ucr)
6. Bureau of Justice Statistics. Retrieved from (https://bjs.ojp.gov/)
7. FBI 2019 Crime Statistics. FBI. Retrieved from (https://ucr.fbi.gov/crime-in-the-u.s/2019/crime-in-the-u.s.-2019/topic-pages/cius-summary)
8. Variables Affecting Crime. FBI. Retrieved from (https://ucr.fbi.gov/hate-crime/2011/resources/variables-affecting-crime)
9. "Dangerous states: Which states have the highest rates of violent crime and most murders?" . USA TODAY. Retrieved from (https://www.usatoday.com/story/money/2020/01/13/most-dangerous-states-in-america-violent-crime-murder-rate/40968963/)
10. Yearbook of Immigration Statistics. Department of Homeland Security. Retrieved from (https://www.dhs.gov/immigration-statistics/yearbook)
11. Climate Monitoring. National Oceanic and Atmospheric Administration. Retrieved from (https://www.ncdc.noaa.gov/climate-monitoring/)
12. FastStats - Marriage and Divorce. Centers for Disease Control and Prevention. Retrieved from (https://www.cdc.gov/nchs/fastats/default.htm)
13. Historical Population Density Data. United States Census Bureau. Retrieved from (https://www.census.gov/data/tables/time-series/dec/density-data-text.html)
14. U.S. Marriage and Divorce Rates by State. United States Census Bureau. Retrieved from (https://www.census.gov/library/visualizations/interactive/marriage-divorce-rates-by-state-2009-2019.html)
15. US records largest annual increase in murders in six decades. Guardian. Retrieved from (https://www.theguardian.com/us-news/2021/sep/27/us-murder-rate-increase-2020)

## <a name="fifteen"> 15. Онлайн-приложения </a>
1. [База данных](Database/)
2. [Архив](Archive/)
3. [Основной датасет](Database/CSV/project_data_full.csv)
4. [Полный разведанализ](Database/PDF/data_analysis_final.pdf)
5. [Описательная статистика](Database/CSV/describe.csv) 
