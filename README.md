# MIST4610Porject1

## Team Name: 
Correlated Subquery 

## Team Members:

1. Spencer Fox [@hhgregg17](https://www.github.com/hhgregg17)
2. 
3. 
4. 
5. 
6. 

## Overview:

Below are 10 queries and a data model covering the many aspects of the NBA. This includes but is not limited to Teams, Players, Statistics, and Transactions. This also includes other relevant infomation about teams and players such as injuries and awards.

## Data Model

Data model explination:

This data model is designed in a way to easily pull statistics from teams, players, and their respective games as well as keeping track of transactions.

The first two entities 'Player' and 'Team' have almost the same aspects. They both have many-to-many relationships to 'Game' via their respective weak entities 'TeamStats' and 'PlayerStats'. Both having two identitfying relationships. Both PlayerStats and TeamStats have many attributes looking into the statistics of singular players and team performance.

Player and Team also have another many-to-many relationship with 'Transactions' though, not identifying. There are two one-to-many relationships with team to keep track of the team the player transfers from and the team they transfer to. 

Player and Team ALSO has a direct one to many relationship. This is to list the players that have never been involved in a transaction.

Player has another two relationships with 'Injury' and 'Awards' (non-identifying) that are one to many. An award/injury can have one player but a player can have many different injuries/awards.

Game has a one-to-many relationship with 'Season' since a season can have many games but a specific game can only be involved with one season.

Lastly there is a many-to-many relationship between 'Coach' and 'Player' via weak entity 'CoachHistory'. A team can have many coaches in the past and a coach could have coached for many teams.

<img width="620" alt="NBAfinalmodel" src="https://github.com/user-attachments/assets/95c38f16-006f-4f58-bddd-6104bad23b92">

