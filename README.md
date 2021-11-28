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
1. [Вводная часть](#one) \
  1.1 [Постановка вопроса](#oneone) \
  1.2 [Постановка гипотезы](#onetwo) \
  1.3 [Теоретическая часть](#onethree) \
  1.4 [Актуальность вопроса](#onefour) 
2. [Описание и разведанализ данных](#two) \
  2.1 [Описание данных](#twoone) \
  2.2 [Разведанализ данных](#twotwo)
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
Чем хуже экономические условия в штате, тем больше в нем происходит насильственных преступлений.

### <a name="onethree"> 1.3 Теоретическая часть </a>
Статистические данные о конкретных преступлениях индексируются в ежегодных [Единообразных отчетах](https://www.fbi.gov/services/cjis/ucr) о преступлениях Федерального бюро расследований (ФБР) и в ежегодных Национальных обзорах виктимизации преступлений, проводимых [Бюро статистики юстиции](https://bjs.ojp.gov/). В дополнение к основному Единому отчету о преступлениях, известному как *Преступность в Соединенных Штатах*, ФБР публикует ежегодные отчеты о состоянии правоохранительных органов в Соединенных Штатах. Содержащиеся в докладе определения конкретных преступлений считаются стандартными многими американскими правоохранительными органами. По данным ФБР, индекс преступности в Соединенные Штаты входят насильственные преступления и имущественные преступления. 

Violent Crimes – насильственные преступления, которые включают: убийство, нападение, непредумышленное убийство, сексуальное насилие, ограбление, угроза, похищение, вымогательство и преследование. 

Согласно статье [«National Crime Rates Compared»](https://web.archive.org/web/20061115003526/http:/www.crimereduction.gov.uk/statistics/statistics35.htm), уровень преступности в Америке по сравнению с другими странами с аналогичным уровнем богатства и развития зависит от характера преступления, используемого при сравнении. Общие сопоставления статистики преступности провести сложно, поскольку определение и классификация преступлений различаются в разных странах.

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

Мы предполагаем, что уровень экономики в штатах США напрямую воздействует на уровень преступности. Так, штаты с ограниченными экономическими возможностями и значительным процентом жителей, испытывающих финансовые трудности, как правило, имеют более высокие уровни насильственных преступлений.  

Мы предполагаем, что уровень экономики в штатах США напрямую воздействует на уровень преступности. Так, штаты с ограниченными экономическими возможностями и значительным процентом жителей, испытывающих финансовые трудности, как правило, имеют более высокие уровни насильственных преступлений, согласно статье [USA Today](https://www.usatoday.com/story/money/2020/01/13/most-dangerous-states-in-america-violent-crime-murder-rate/40968963/).

Чтобы говорить об экономике в целом, мы выделили основные показатели, такие как: **доход, ВВП, уровни безработицы и бедности**.  

Также можно сделать теоретические предположения, как эти показатели влияют на основную характеристику. Недостаточный уровень дохода является побудительным фактором для таких преступлений как ограбление и вымогательство, которые в свою очередь могут быть причиной нападения и даже убийства. Если говорить об уровне бедности, то люди за чертой бедности предположительно используют более жесткие методы обогащения, так как им нужно не просто найти дополнительный «заработок», а в целом найти средства существования, в таком случае можно говорить о преднамеренных убийствах ради наживы. Это лишь малейшая часть конкретных предположений, которые относятся далеко не ко всем преступлениям. Чтобы подробно изучить зависимость факторов в целом, мы будем исследовать данные за несколько лет в разных штатах, проверив таким образом нашу гипотезу.  

### <a name="onefour"> 1.4 Актуальность вопроса </a>
Нам кажется, что данный вопрос особенно актуален в современной Америке - страна пребывает в состоянии роста насильственной преступности. Тому подтверждение статья Guardian о небывалом росте убийств:  
> As a country, as a society, we don’t have a great answer to that, but we need to be trying, and innovating, and we need to be taking it [the problem of rising violence] seriously.  
>
Помимо этого, рост насильственной преступности - одна из важнейших политических тем, составляющая дебатов Республиканцев и Демократов, причина различных митингов. Нам кажется, что опыт подобного исследования может содействовать снижению роста преступности и повышению осведомленности о наиболее вероятных признаках надвигающейся угрозы.

О влиянии преступности на социально-экономическое развитие страны говорится в статье [“Impacts of Crime on Socio-Economic Development”](https://www.researchgate.net/publication/354382389_Impacts_of_Crime_on_Socio-Economic_Development). Преступность часто является препятствием на пути социально-экономического роста общества, препятствует инвестициям, увеличивает стоимость транзакций и, в конечном итоге, способствует миграции, которая в конечном итоге создает диспропорции в экономическом развитии во всем мире.

Наше исследование актуально, потому что оно покажет зависимость экономических условий штата и уровня преступности, что в свою очередь позволит сделать вывод о важности экономического роста и преодолении безработицы при борьбе с преступностью. 

## <a name="two"> 2. Описание данных, разведанализ данных </a>
### <a name="twoone"> 2.1 Описание переменных </a>
+ Vcrime - количество совершенных насильственных преступлений на 100 тысяч населения. 
+ PIPC - personal income per capita, all states. 
+ RGDP - real GDP, all industry, all states. 
+ UR - unemployment rate, all states. 
+ PR - poverty rate, according to Poverty Level. 

### <a name="twotwo"> 2.2 Разведанализ данных </a>
В нашем исследовании мы используем данные по **50 штатам США с 2010 по 2019 год.**

Чтобы изучить экономические условия штата, мы включили такие характеристики как количество совершенных насильственных преступлений, уровень бедности и безработицы, а также доход и реальный ВВП.

[Предварительный просмотр данных.](/project_data_new.csv) 

#### Рассмотрим переменные более подробно:  
Для подробного анализа мы также проверили корреляцию между зависимой переменной Vcrime и объясняющими переменными:

![State Description](/Database/Images/corr_vcrime.png)

#### Переменная State. 
![State Description](/Database/Images/state_desc.png)\
Текстовая переменная, обозначающая название штата, имеющая [50 уникальных значений](/Database/Images/state_unique.png)

#### Переменная Vcrime. 
![Crimes Description](/Database/Images/crimes_desc.png)\
Числовая переменная, указывающий количество совершенных насильственных преступлений (violent crimes) на 100 тысяч населения. Значения колеблются в диапазоне от 122 до 703, где среднее (363) и медианное (337) близки друг к другу.

Мы построили [график](/Database/Images/crimes.png), который показывает количество наблюдений и их плотность в стране. Таким образом выяснили, что количество регистрируемых наблюдений в целом находится на достаточно высоком уровне, что еще раз подтверждает выводы СМИ о существующей проблеме с насильственными преступлениями на территории Соединенных Штатов Америки.

#### Переменная PR. 
![Poverty Rate Description](/Database/Images/pr_desc.png)\
Poverty rate - числовая переменная, обозначающая уровень бедности в долях, то есть от 0 до 1. В нашем случае минимальное значение 0.0818, а максимальное 0.2173.

Коэффициент корреляции с переменной Vcrime и коэффициенты [парной линейной регрессии](/Database/Images/regr_PR.png) указывают на значимость взаимосвязи между этими переменными.

Этот тренд мы можем заметить и на [графике рассеивания](/Database/Images/dispPR.png).

Данные мы дополнительно проверили на отсутсвие [гетероскедастичности](/Database/Images/BP_PR.png).

Почти все штаты показывают неплохие - относительно мировых - результаты по уровню бедности. Тем не менее, есть штаты, которые за десять лет наблюдений все так же имеют достаточно высокую (близко к 0.2 и выше) долю населения, находящегося за чертой бедности. Это может объясняться локальными экономическими, географическими и климатическими особенностями, которые мешают развитию штата.

#### Переменная UR.
![Unemployment Rate Description](/Database/Images/ur_desc.png)\
Unemployment rate - уровень безработицы в штатах в долях. Значения колеблются от 2,9% до 8,3%. 

Коэффициенты корреляции и [парной линейной регрессии](/Database/Images/regr_UR.png) с переменной Vcrime показывают наличие значимости взаимосвязи между переменными.

На графике вида [scatter plot](/Database/Images/dispUR.png) действительно можно наблюдать некоторую зависимость. 

Также мы проверили данные на отсутствие [гетероскедастичности](/Database/Images/BP_UR.png).

Следует также заметить, что уровень безработицы в США в среднем держится на оптимальном уровне, потому что падения ниже 5%, как правило, приводят к снижению общего уровня выпуска и усилению инфляции. Подобные значения также говорят об эффективности работы Федеральной Резервной Системы.

#### Переменная PIPC. 
![Personal income per capita Description](/Database/Images/pipc_desc.png)\
Personal income per capita - числовое значение, выражающее доход на душу населения в долларах. Максимальное значение (67553) более чем в два раза больше минимального (35163), хотя среднее и медианное значения чуть больше 45000. Таким образом значений, близких к максимальному, довольно мало. 

Коэффициент корреляции с Vcrime слишком мал, а значение [p-value](/Database/Images/regr_PIPC.png) в парной регрессии слишком велико, чтобы говорить о сильной значимости взаимосвязи переменных. Мы предположили, что есть некоторые выбросы, мешающие анализу и действительно увидели это на графике типа [boxplot](/Database/Images/boxplotPIPC.png). Это доходы жителей штата Коннектикут, которые достигают 67.5 тысяч, учитывая что уровень дохода на душу населения приходится в основном на промежуток от 43 до 51 тысячи долларов на душу населения. 

Выбросы можно объяснить спецификой данного показателя: он фиксирует все доходы человека (зарплата, доходы от аренды, дивиденды, трансферты и другие виды). Однако в данном случае это может влиять на корреляцию между переменными, так что попробуем прологарифмировать значение PIPC. Логарифм делает показатели относительными, что позволяет избавиться от [выбросов](/Database/Images/boxplotlogPIPC.png).

К сожалению, увеличить значимость при этом не удалось. Показатель [p-value](/Database/Images/regr_PIPC2.png) сдвинулся в меньшую сторону совсем мало, а [показатель корреляции](/Database/Images/corr_logPIPC.png) в свою очерель поменял знак, но по модолю чуть увеличился. Поэтому в дальнейшем все-таки будем использовать именно логарифм дохода населения. Также данные  были проверы на наличие [гомоскедастичности](/Database/Images/BR_PIPC.png).

В рамках показателя Personal Income per Capita наблюдается положительная тенденция: усреднённые за 10 лет данные показывают, что доход на душу населения находится на достаточно высоком уровне почти во все штатах, что свидетельствует о приемлемом состоянии экономики. Кроме того, следует отметить, что подобные показатели достигаются, в том числе, благодаря западной контрактной системе с фиксированными почасовыми ставками.

#### Переменная RGDP.
![Real GDP Description](/Database/Images/rgdp_desc.png)\
Real GDP - числовое значение реального ВВП штата. За 10 лет он находится в среднем в пределах от 29180 до 2335826. 

Аналогично предыдущему результату нельзя говорить о значимости переменной из-за низкого коэффициента корреляции и большого p-value в [парной регрессии](/Database/Images/regr_RGDP.png).

Максимальное значение в данном случае 2335826, а значение 3го квартиля - 442790. Это говорит об очень сильных выбросах. Мы рассмотрели график [boxplot](/Database/Images/boxplotRGDP.png) для проверки и увидели 3 выброса данных. Это [3 штата](/Database/Images/highRGDP.png) - Калифорния, Техас и Нью-Йорк, которые отличаются от других штатов тем, что средний реальный ВВП с 2010 по 2019 год был выше 1300000, а у остальных штатов значительно ниже. Однако эти выбросы снова могут отрицательно повлиять на наши будущие оценки, поэтому логарифмируем переменную. Это позволило избавится от [выбросов](/Database/Images/boxplotlogRGDP.png).

Если говорить о числовых [показателях](/Database/Images/regr_logRGDP.png), то нельзя сказать, что данные значительно изменились, но все же [показатели](/Database/Images/corr_logRGDP.png) стали ближе к тем, что гарантируют значимость. Именно поэтому мы будем использовать логарифм уровня ВВП в дальнейшей модели. Новые показатели мы проверили на наличие гомоскедастичности, гипотеза отвергнута из-за низкого p-value - данные [гетероскедастичны](/Database/Images/BR_RGDP.png), поэтому при построении модели будут использованы робастные ошибки.

В рамках показателя Real GDP наблюдается тенденция к росту показателя в зависимости от размера и численности населения штата, его ранга бизнес-среды, скопления высокотехнологичных производств и размерности рынка венчурного капитала.

**Полный разведанализ** можно прочитать здесь: [pdf файл](/data_analysis_new.pdf)\
**Код разведанализа** можно найти здесь: [rmd файл](/data_analysis_new.Rmd)

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
+ Содержательная постановка: при прочих равных уровень насильственных преступлений в штате не зависит от уровня бедности, безработицы, дохода на душу населения и ВВП
+ Гипотеза в нормальной форме: 
```
Ho: {β1 = 0;
     β2 = 0;
     β3 = 0;
     β4 = 0}

Ha: {Ho неверна}
```


## <a name="four"> 4. Ожидаемые результаты </a>

Мы предполагаем, что существует прямая зависимость между уровнем бедности и безработицы и количеством преступлений в штате. Также мы думаем, что чем ниже реальный ВВП и доход на душу населения в штате, тем больше в нем совершают насильственные преступления. Как итог, мы ожидаем получить результаты исследования, позволяющие утверждать, что зависимость между экономическим состоянием штата и уровнем насильственных преступлений в нем существует.

## <a name="five"> 5. Результаты регрессионного анализа </a>

[Полноценные результаты регрессионного анализа](/Database/Images/regress_res.png) 

+ В нашей модели мы приняли решение прологарифмировать переменные PIPC и RGDP из-за наличия выбросов и большого разброса значений. 
+ Также из-за наличия гетероскедастичности в переменной RGDP мы рассчитали робастные оценки.
+ Согласно нашей модели, на уровне значимости 5% значимой является только переменная, содержащая информацию об уровне бедности.
+ Затем мы провели несколько тестов Вальда для проверки гипотезы и они подтвердили наши результаты: **нулевая гипотеза отвергается только для переменной PR**.

## <a name="six"> 6. Анализ результатов </a>

В результате [нашего исследования](/Database/Images/walds.png) мы выяснили, что на количество насильственных преступлений в штате из всех факторов, исследуемых нами, влияние оказывает только уровень бедности (PR).
Мы предполагаем, что такой результат обосновывается тем, что бедность является сильнейшим детерминантом преступности. 
Прежде всего внутреннее состояние личности, внешне выраженное в бедности, влияет на психологическое развитие и нравственные ориентиры. В социуме считается, что быть бедным - значит быть человеком, который не состоялся в жизни, саму же бедность определяют как неудовлетворительное качество жизни и осознание своего положения, которое, в дальнейшем, при сравнении с другими людьми вызывает досаду. Люди, которые постоянно находятся в нужде, начинают думать только о решении своих бытовых проблем (еда, одежда, кров). В связи с этим накапливаются обиды, неудовлетворенность становится обыденностью, что в дальнейшем приводит к противопоставлению себя социуму, девиантному поведению и желанию решить финансовые проблемы, прибегнув к совершению преступлений.

Что касается переменных не оказавших влияние на уровень преступности в штате: ситуация с безработицей в США в целом находится под контролем государства. Благодаря сильной социальной поддержке, безработные практически ни в чём не нуждаются. Даже минимально гарантированный уровень социальной помощи обеспечивает нормальную жизнь – без излишеств, но умеренно комфортную. В связи с этим мы можем утверждать, что отсутствие работы у индивида в США зачастую не означает его нужду в деньгах или наличие проблем в социальной сфере, что бы могло сподвигнуть его к совершению преступлений.

Такие переменные как доход на душу населения и реальный ВВП скорее определяют уровень экономического развития штата в целом. Слабая сторона применения данных показателей в качестве критерия благосостояния штата выражается в отсутствии учета диспропорций при распределении доходов. Ко всему прочему, доход на душу населения не учитывает имеющиеся сбережения населения и капитал. Анализируя данные переменные, сложно утверждать о наличии и количестве в штате лиц за чертой бедности, склонных к преступлениям.

## <a name="seven"> 7. Ответ на содержательный вопрос в рамках проведенного анализа </a>

В результате исследования мы выяснили, что **существует зависимость между уровнем бедности и количеством насильственных преступлени**й, в то же время, такие переменные, как ВВП, доход на душу населения и уровень безработицы **существенного влияния** на количество насильственных преступлений **не оказывают**. Поскольку экономическое состояние штата описывается не одной переменной, а несколькими разными, о конкретной зависимости между ним (экономическим состоянием штата) и количеством насильственных преступлений **утверждать нельзя**.

## <a name="eight"> 8. Критический анализ результатов и анализ ограничений исследования </a>

## <a name="nine"> 9. Предложения по возможному расширению исследования </a>

## <a name="ten"> 10. Заключение </a>

## <a name="eleven"> 11. Вклад членов команды в групповую работу </a>
|  	| Федоров  Д.А. 	| Дасмаева М.В. 	| Клечикова М.А. 	| Рахманова А.Ф. 	| Жигульская Е.Л. 	| Струговец М. 	| Бухановская Ю.А. 	|
|:---:	|:---:	|:---:	|:---:	|:---:	|:---:	|:---:	|:---:	|
| Оценка 1 	|  ---|  	|  	|  	|  	|  	|  	|
| Оценка 2 	|  	| --- 	|  	|  	|  	|  	|  	|
| Оценка 3 	|  	|  	| --- 	|  	|  	|  	|  	|
| Оценка 4 	|  	|  	|  	| --- 	|  	|  	|  	|
| Оценка 5 	|  	|  	|  	|  	| --- 	|  	|  	|
| Оценка 6 	|  	|  	|  	|  	|  	| --- 	|  	|
| Оценка 7 	|  	|  	|  	|  	|  	|  	| --- 	|

## <a name="twelve"> 12. Приложения с техническими результатами </a>

## <a name="thirteen"> 13. Приложения с кодами </a>

[Код для проведения регрессионного анализа и статистических тестов](/regression.Rmd)

[Результаты статистических тестов](/Database/Images/walds.png)

## <a name="fourteen"> 14. Источники </a>
1. United Health Foundation, National Violent Crime Data. America’s Health Rankings. Retrieved from https://www.americashealthrankings.org/explore/annual/measure/Crime/state/ALL?edition-year=2020 
2. Local Area Unemployment Statistics. U.S. Bureau of Labor Statistics. Retrieved from https://www.bls.gov/lau/ 
3. Economic Data, Per Capita Personal Income, Real GDP. FRED. Retrieved from https://fred.stlouisfed.org/ 
4. Distribution of Total Population by Federal Poverty Level. KFF. Retrieved from https://www.kff.org/state-category/demographics-and-the-economy/people-in-poverty/ 

## <a name="fifteen"> 15. Онлайн-приложения </a>
1. [Основной датасет](/project_data.csv)
2. [База данных с исходниками](/Database)
3. [Разведанализ](/data_analysis.pdf) 
