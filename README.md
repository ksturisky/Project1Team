
# MIST4610 Project 1






## Team Name

CRN Group 1
## Team Members

1. Jake Bogartz @jab9323
2. Aiden Abramawitz @aja1232
3. Max Young @mxgyoung
4. Kiefer Sturisky @ksturisky
## Problem Description

The given problem is to create a database for an owner of a football team that models the entities and relationships that exist. We decided to improve the model by portraying the entities and relationships of an entire football league. The central entity of the model is Team, which represents each of the competing teams in our league. The team entity is then related to the players on the roster, the staff that works for them, the fans that cheer for them, their  
financial situation, and the results of each game they play in. Furthermore, we are looking to expand on the game entity by connecting it to entities that record player statistics within a game, injuries that occur, and the amount of games within a given season. Finally, we are including an awards entity to capture the best players from a given season. Our goal is to accurately model the relationships between these entities, insert sample data into each entity, and execute functioning queries in order to provide us with valuable information about our created football league.
## Data Model

Explanation of Data Model:
Our model is based on the structure of a created football league. The central entity, Team, includes information about the name of the team and where it is located. Within each team, there are many players, staff members, and fans, which explains the many to many relationships that exist between Team and the Player, Staff and Fan entities. Within the player entity, we capture the name, date of birth, and position of each individual. Within the staff entity, we include information on their name, job position, and salary. Furthermore, we implemented a recursive relationship within the staff entity in order to define who is the respective boss of each of the staff members. The fan entity includes information on their name, contact info, and season ticket status. 

Additionally, each team has different types of financial transactions they’re related to, which is why we created a one to many relationship between Team and Financials. The Financials entity includes other information such as the type of transaction, the amount, and the date that it takes place. The final relationship that takes place with the team entity is between Team and Game. Each team plays in many games which lead to using a many to many relationship to connect the entities. This relationship allows us to record which teams are playing in each game, what season it is taking place in, and the outcome of the game.

The Game entity has three other branches coming off of it, connecting to entities representing Statistics, Injuries, and Season. Within each game, there are many different statistics that can be recorded, however, a player can only record one of each type of statistic in a given game, leading to a one to one relationship. The statistics entity also records the type of statistic being logged, the value of the statistic, and which player the statistic correlates too. Similarly, there are many different injuries that can take place within a single game. Unlike statistics, it is possible for a player to have the same injury twice in a given game, leading to another one to many relationship. The Injuries entity records information on what type of injury occurred, to which player, and which game. The final branch that comes out of the game entity is in relation to the season entity. Although a season has many games, each game is identified by a unique number, making it impossible to have a repeating game ID. This means that the relationship between the two entities is one to one. Furthermore, we included information in the Season entity to capture the start and end dates of the given season.

The final relationships that take place within our model involve the Awards entity. The awards entity has a one to many relationship with season, since there are a number of different awards that are given out on any given season. The awards entity contains information on the name of the award, which player won the award, and in which season it was awarded. The other branch that Awards is related to is Player. Since it is impossible for a player to win the same award twice in the same season, a one to one relationship is used.
