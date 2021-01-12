# Набор данных, содержащий информацию о кризисах, астрономических событиях и пророчествах с января 1915г по октябрь 2020г
Содежит информацию о цене золота, банковских кризисах, лунных затмениях, солнечных циклах, ретроградности планет и предсказаний Ванги и пророчеств второго пришествия христа, ВВП стран и уровня убийст.

Поможет исследователям проверить гипотезы:
- взаимосвязи кризисов и астрономических событий
- взаимосвязи кризисов и пророчеств 
- взаимосвязи пророчеств и астрономических событий
- взаимосвязи между кризисами в различных странах, ценами на золото, уровнями убийст и ВВп

## Команда:
- Лушпина Екатерина
- Сухоносенко Анастасия
- Авдеева Наталья
- Кудрявцев Александр
- Саид Абдулахатов


### Источники данных:

* [Лунные затмения, новолуния, полнолуния](https://rhodesmill.org/pyephem/)
* [Циклы солнечных активностей](https://en.wikipedia.org/wiki/List_of_solar_cycles)
* [Солнечные затмения](https://eclipse.gsfc.nasa.gov/SEsearch/SEsearch.php)
* [Данные о ретроградности планет](https://ru.astro-seek.com/retrogradnye-planety-astro-kalendar-1925)
* [Данные о кризисах](https://www.hbs.edu/behavioral-finance-and-financial-stability/data/Pages/global.aspx)
* [Пророчества 2го пришествия Христа](https://en.wikipedia.org/wiki/Predictions_and_claims_for_the_Second_Coming_of_Christ)
* [Предсказания Ванги](http://www.vizagchemical.com/blog/list-baba-vanga-predictions-info-chemical-man)
* [Цена золота](https://www.macrotrends.net/1333/historical-gold-prices-100-year-chart)
* [ВВП стран](https://www.rug.nl/ggdc/historicaldevelopment/maddison)
* [Уровень убийств в странах](http://www.cgeh.nl/data#homicide)


# [Итоговый набор данных](https://github.com/NeznaikanaLune/MISIS_DS_Masters_degree_2020/blob/master/internal_competitions/01_semester/misis_dataton2020/data_storage/astro_crisis_predictions_set.csv)
Размер итогового набора данных:
- строк 1270
- столбцов 54

## Описание набора данных

| Название столбца  | Тип данных |  Значение |  Описание |
| ------------- | ------------- | ------------- |------------ |
| date  | str  |даты с 1915 по. окт 2020   |  |
| date_dt  | datetime  |даты с янв 1915 по. окт 2020   |  |
| solar_cycle  | int  |(0,15,16,17,18,19,20,21,22,23,24) | Циклы солнечной активности. 0 -нет цикла, [15:24] - номер цикла  |
| solar_eclipse | int()|[1,2,3],1-annular,2-total,3-hybrid|![](https://miro.medium.com/max/886/1*4r-zzhll42AeSyc1vqCykQ.jpeg)|
| full_moon_eclipse  | int |(1,0 binary)  | Полные лунные затмения.1-затмений,0-нет затемения |
| full_moon  | int |[1,2,3,4,5]| Количество полнолуний в месяце |
| new_moon  | int| [1,2,3,4,5]  | Количество новолуний в месяце |
| gold_price  | float| | Цена золота (с поправкой на инфляцию)за унцию|
| vanga_descriptions  | str| | Предсказания Ванги  |
| vanga_binary  | int| (1,0 binary) | Предсказания Ванги  |
| score_google  | float| [-1,1] | Google Cloud Natural Language API общая оценка эмоциональности -1 негативное,0 нейтрально, 1 позитивно  |
| magnitude_google  | float| [0,+inf] | Google Cloud Natural Language API указывает на общую силу эмоций (как положительных, так и отрицательных)  |
| sentiment_aws  | float| ['NEGATIVE','NEUTRAL','POSITIVE'] | Amazon Language API категориальная оценка эмоциональности|
| second_coming_of_christ | int| (1,0 binary)|Предсказания 2го пришествия Христа  |


Для Меркурия, Венеры, Марса, Юпитера, Сатурна, Урана, Нептуна, Плутона:
| Название столбца  | Тип данных |  Значение |  Описание |
| ------------- | ------------- | ------------- |------------ |
| planet_name_retro  | int| (1,0 binary)| Ретроградное движение планет |


Для  Франции, Германии, Испании, Великобритании, США:

| Название столбца  | Тип данных |  Значение |  Описание |
| ------------- | ------------- | ------------- |------------ |
| banking_crisis  | int|(1,0 binary)| Банковский кризис  |
| currency_crisis  | int|(1,0 binary)| Валютный кризис  |
| independence  | int|(1,0 binary) | Независимость  |
| inflation_crisis  | int|(1,0 binary) | Кризис инфляции  |
| systemic_crisis  | int|(1,0 binary)| Системный кризис  |
| cgdppc  | int|(1,0 binary)|  ВВП на душу населения. Выражается в долларах США 2011 года с поправкой на инфляцию в Соединенных Штатах |
| rgdpnapc  | int|(1,0 binary)| Реальный ВВП на душу населения. Отслеживает темпы роста ВВП на душу населения, приведенные в национальных счетах стран (или их исторических реконструкциях). Выражается в долларах США 2011 года|
| homicide_rate  | float||  преднамеренные убийства, умышленно причиненная одному человеку другим человеком – измеряется в количестве смертей на 100 000 жителей |

# Доп инфо

[**Код для выгрузки данных**](https://github.com/NeznaikanaLune/misis_dataton2020/blob/main/data_storage/Nostradamus%20.ipynb)

<p><b>Дата создания:</b>  23-10-2020</p>
<p><b>Дата обновления:</b> 23-10-2020</p>

<b>license:</b> Creative Commons Public Domain Dedication

[**Ссылка на отдельные наборы данных, из которых составлен итоговый набор данных**](https://github.com/NeznaikanaLune/misis_dataton2020/tree/main/data_storage/sub_data)

