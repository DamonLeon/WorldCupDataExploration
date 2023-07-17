# World Cup Data Exploration


# Description
An exploration of the FIFA World Cup 2022 in Qatar, looking at visualising the performance of each team and head to head match ups. This project involved taking some initial data, cleaning and wrangling it into an appropriate format before turning it into a data visualisation.


Three visualisations were made in Tableau using the processed data, and published in Tableau Public:

## Team Summary

- Dashboard looking at the team's tournament performance, their game match ups and furthest stage of the tournament and a map
- https://public.tableau.com/app/profile/damon.leon/viz/QatarWorldCup2022TeamSummary/TeamSummary

- ![image](https://github.com/DamonLeon/WorldCupDataExploration/assets/87230042/dc4e7a69-c134-43c3-b7cc-b323b692d7ab)



## Game Summary

- Dashboard where the user can specify a specific match result they want to analyse, relaying the relevant head to head statistics
- https://public.tableau.com/app/profile/damon.leon/viz/QatarWorldCup2022GameSummary/GameSummary
![image](https://github.com/DamonLeon/WorldCupDataExploration/assets/87230042/58f83b81-78da-4253-ad58-5dd277f46602)


## Goals Scored vs Conceded

- Analytic on average team performance over the tournament, looking at average goals scored vs average goals conceded
- https://public.tableau.com/app/profile/damon.leon/viz/WorldCupScoredvsConcededv1/AverageGoalsConceded_1
- ![image](https://github.com/DamonLeon/WorldCupDataExploration/assets/87230042/a765945f-7b10-4067-919a-4e08e7b7af49)








# Data Source

https://www.kaggle.com/datasets/die9origephit/fifa-world-cup-2022-complete-dataset

# Data Wrangling
Although the data is relatively clean, there was still some pre processing and wrangling to be done to get the data in an appropriate format for the visualisations. The work for this was performed in the Jupyter Notebook (World Cup Analysis.ipynb).


# Data Export
After wrangling, the additional features/formatted data was exported to .csv files to fed into Tableau. These were

- final_scores.csv
- groups_furthest_stages.csv
- locations.csv
- played_scored_conceded.csv
- total_cards.csv


# Tableau Workings
Both the initial data and additional .csv files were then added into Tableau to make the three visualisations. The Tableau workbook is also tracked within this repository (Qatar World Cup 2022 Visualisations.twb)


# Learnings

Data Wrangling: 

- Using pandas for general data manipulation, data cleaning and feature engineering
- Using matplotlib to create basic graphs for sense checks and ensuring 
- Using geopy to feed in a country's name and get their location (longitude/latitude) to add into their 


Tableau:
- Visualisations basics - keeping the scales the same for graphs, being intentional with colour choices, using labels and colour to highlight min/max,
- Creating custom colour filters (the team name and colour of map marker in Team Summary corresponds with either the team's national flag/kit). 
- Making interactive drop down filters that can control the whole dashboard, such that the dashboard changes dynamically. 



# Future Improvements / Next Steps

- Making team1 and team 2 selection work in both directions - due to the way the data is initially structured, the relevant teams are only returned once team1 has been selected (i.e you can't start off selecting team2 first then team1) . In some instances, this has the effect that it looks as if a team has only played one game (e.g Australia as team 1, Denmark as team2), but this is just the result of how the data is initially structured and all games played in the tournament are captured in the dashboard. 

- Adding each team/country's flag as an image that dynamically changes with the team selection - I wasn't able to find an easy way to do this as Tableau doesnt seem to have a native feature to support this functionality. Would be nice just for aesthetics if anything


- I would have loved to include player data under Team Summary to include things like standout players and top scorers. It also would have been nice to have data to show which player scored and at what minute in the game, which is something commonly included in most match summaries. 

- The visualisation doesn't give a clear indication of who won the game if the game went to penalties (e.g the Argentina vs France final), since the data I have doesn't include penalty shootout data. 


# Acknowledgements


### Inspiration
Credit to Kim Tricker's visualisation for some intial inspiration for the visualisations
https://public.tableau.com/app/profile/kim.tricker/viz/WorldCupBeginnersGuide/WorldCupBeginnersGuide

### Data Source
https://www.kaggle.com/datasets/die9origephit/fifa-world-cup-2022-complete-dataset

