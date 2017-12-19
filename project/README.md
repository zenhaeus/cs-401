# Applied Data Analysis - Project

Notebook best viewed on: [NBViewer](http://nbviewer.jupyter.org/github/zenhaeus/cs-401/blob/master/project/Project%20-%20report.ipynb)

## Abstract

The age of information makes it seem as though conflict and wars are, and always will be, ever growing part of our lives. We often feel overwhelmed by the amount and scope of information that is accessible and directed towards us, in turn rendering us indifferent to the consequences and casualties of the war.

Civilians are the greatest casualty of any war, and casualties are not always measured in body count. Civil liberties and political freedoms are and should be enjoyed by the people from all around the world, and conflicts always bring changes to freedom of expression, for better or worse.

In this project we want to focus on the continent of Africa, which we feel is underreported in the context of occurring conflicts and casualties. We will utilize UDCP dataset documenting individual events of organized violence, empowered by the Freedom House 'Freedom in the World' yearly surveys and the Human Development Index as measured by the UN.

Our goal is to produce a report with an overarching story about impacts of conflicts on the African continent in the observed period from 1990 to 2015, with the focus on civilian populations - what are the long term consequences that conflicts have on the development of the civilian population.

## Research questions

* Is conflict frequency and impact negatively correlated with the HDI and the state of human rights in the African nations?
* How are different types of conflict impacting HDI and the state of human rights in the African nation?
* Does peacetime result in growth of HDI and improvement of political and personal liberties? If so, what is the nature of growth over time?

Possible case studies:

* Some African countries have been ruled by dictators under fake cover of the democratic system for long periods of time, so political and personal liberties could have actually deteriorated, while HDI could have steadily grown. We would present a country like Zimbabwe in this context as a type of small case study, where we would provide additional context regarding the political climate throughout observed time period.

## Dataset

1. Uppsala Conflict Data Program's georeferenced event dataset, [Global Version 17.1 (2016)](http://www.ucdp.uu.se/downloads/ged/ged171-xlsx.zip), is the central dataset used in our project. Dataset covers individual events of organized violence - phenomena of lethal violence occurring at a given time and place. There are 135,181 events present in the dataset covering the entirety of the Globe (excluding Syria), spanning from 01/01/1989 to 31/12/2016. This project makes use of the events which occurred on the African continent throughout the period of 26 years (1990-2015), or roughly 35,437 events. Events documented in the dataset will be aggregated by region, and together with information about the Human Development Index (HDI), Political Freedom score and Civil Liberties score, further analyzed and visualized on per-region basis.

1. Freedom House is a U.S.-based U.S. Government-funded non-governmental organization (NGO) that conducts research and advocacy on democracy, political freedom, and human rights. The organization's annual *Freedom in the World* reports on the state of political freedoms and civil liberties enjoyed in different countries form our second dataset and can be obtained [here](https://freedomhouse.org/sites/default/files/FIW2017_Data.zip). We will focus our attention on the file `FH_Country_and_Territory_Ratings_and_Statuses_1972-2016.xls` which contains information about political freedom and civil liberties scores for individual countries throughout the period of 1972-2016. Moreover, we are only interested in the scores of African countries throughout the period of 1990-2015.

1. The Human Development Index (HDI) is a composite statistic (composite index) of life expectancy, education, and per capita income indicators, which are used to rank countries into four tiers of human development. A country scores higher HDI when the lifespan is higher, the education level is higher, and the GDP per capita is higher. Our final dataset is Human Development report by the UN that includes calculated Human Development Indices for the years 1990 through 2015. Naturally, we are interested in the values associated countries from the African continent. Human Development Index obtains value in the range [0,1], 1 being best possible value.

More detailed discussion on the values present and assumptions introduced by these datasets can be found in project's notebook.

## Contributions by the group members
Hrvoje Busic

* Problem formulation, project planning and workload distribution
* map visualizations with interactive elements
* report proofreading.

Domenica Verbaro

* Crawling the data
* data pruning
* data visualization via plots
* report visualizations.

Joey Zenhäusern

* Code modularization and pruning
* writing up the report
* reference checkup.
