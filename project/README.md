# Applied Data Analysis - Project Milestone 1

## Abstract

The age of information makes it seem as though conflict and wars are, and will be, ever growing part of our lives. In this project we will analyze a dataset containing over 135,000 geolocated entries about conflicts between different parties, ranging from the year of 1990,  to the year of 2016.

We will answer some questions about the nature of conflicts that have occurred during the life of an average EPFL student. We will explore what parties have been most involved in the conflicts and how often are certain regions involved in the conflicts. Furthermore, we will aim to observe significant changes through certain time periods with regard to frequency of conflicts and their location. Finally, we will conduct thorough statistical analysis of relevant characteristics of said conflicts.

The goal of our project is to use accompanied exhaustive data set to provide a better understanding of the conflicts through their types, relevant characteristics and locations.

## Research questions

Statistical analysis that will dive deeper to the regional level as the data shows to be more relevant for certain regions:

* Biggest actors in terms of:
    * Number of conflicts for one party
    * Number of conflicts between two parties
* Death toll:
    * In a prolonged conflict between parties
    * In a single incident
    * By time period

Exploratory analysis:

* What are the parties that are engaged in the conflict, and what is the duration of the conflict in question (violent incident     prolonged war campaign etc.)?
* Exploration of the geographical proximity of the events that took place through regions in which they happened.
* Exploration of changes in the conflict frequency in regards to types of warring parties and region.

Questions that will be further discussed, and included if appropriate:

* Can alliances be inferred from the data?
* Can the available data about the conflicts be connected with the economic context of the warring parties in a meaningful way?


## Dataset

We decided to use the UCDP Georeferenced Event Dataset (GED) Global version 17.1(2016) for our project.
Data set description present on the website gives us a better understanding of the data present: ‘The basic unit of analysis for the UCDP GED dataset is the ‘event’, i.e. an individual incident (phenomenon) of lethal violence occurring at a given time and place. More specifically, we define an event as: ‘An incident where armed force was by an organised actor against another organized actor, or against civilians, resulting in at least 1 direct death at a specific location and a specific date’. The dataset contains 135,181 events. GED 17.1 is a global dataset that covers the entirety of the Globe (excluding Syria) between 1989-01-01 and 2016-12-31.’ (ref. ‘Sundberg, Ralph, and Erik Melander, 2013, “Introducing the UCDP Georeferenced Event Dataset”, Journal of Peace Research, vol.50, no.4, 523-532’).

We can download the dataset in xlsx format from the [website](http://ucdp.uu.se/downloads/) and at first look we see that it contains all the data that expected for our analysis. At this stage of the project, data set has not been enriched or otherwise altered for further analysis.

Some of the attributes that we will use and want to highlight are:

* ‘year’ - identifies the year of the event
* ‘type_of_violence’ - represents the type of conflict (e.g. state based or one-sided violence)
* ‘side_a_new_id’ and ‘side_b_new_id’ - attributes that indicate the two actors of the conflict
* ‘latitude‘, ‘longitude’ - identify where the conflicts took place

## A list of internal milestones up until project milestone 2

1. Wednesday, November 10th:
    * Data import, cleansing and parsing into appropriate formats.
    * Consideration of statistics that will be used throughout the project.
    * Consideration and discussion about libraries that will be used throughout the project.

2. Wednesday, November 17th:
    * Understanding of the data distribution. 
    * Calculating statistics, correlations and appropriate plots.

3. Wednesday, November 24th:
    * Focus on data visualization with emphasis on map visualization.

## Questions for TAs

Does the overarching story behind the project need to also be present inside the Jupyter notebook with all the code.
