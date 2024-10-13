# MIST4610Porject1

## Team Name: 
Correlated Subquery 

## Team Members:

1. Spencer Fox [@hhgregg17](https://www.github.com/hhgregg17)
2. Farzaan Hemani [@Frh53839](https://github.com/Frh53839)
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

## Data Dictionary:

![Screenshot 2024-10-04 135531](https://github.com/user-attachments/assets/dc18d126-08d0-4a3d-8f0c-502596c84b68)

![Screenshot 2024-10-04 135550](https://github.com/user-attachments/assets/57587976-4a84-4715-a228-f8838a289649)

![Screenshot 2024-10-04 135607](https://github.com/user-attachments/assets/33effcc2-3a7b-4133-aa6c-69f7504d74a9)

![Screenshot 2024-10-04 135624](https://github.com/user-attachments/assets/3b589769-26e1-46cf-bf54-eb759f81157c)

![Screenshot 2024-10-04 135656](https://github.com/user-attachments/assets/405a5cd1-385d-4cf5-91d4-768ba3d57463)

![Screenshot 2024-10-04 135710](https://github.com/user-attachments/assets/6b0a8ff5-2cf4-44de-aacd-1eb06ac7b89b)

![Screenshot 2024-10-04 135724](https://github.com/user-attachments/assets/18385b42-f73d-4278-bf19-88183db5d559)

![Screenshot 2024-10-04 135740](https://github.com/user-attachments/assets/2eb3fc84-18bb-4154-a53e-1e6ed41c87ab)

![Screenshot 2024-10-04 135751](https://github.com/user-attachments/assets/dbe882b5-e87c-497f-a123-9e7c45347045)

![Screenshot 2024-10-04 135803](https://github.com/user-attachments/assets/d5a6aade-4e96-469a-a08d-7439a8bb0f12)

![Screenshot 2024-10-04 135819](https://github.com/user-attachments/assets/3b5d8265-f34b-410a-a78f-e9c97a5e8a80)

## Queries:


1. Query 1 gives us the number of assists and average points scored per game while having more than 5 assists and over an average of 20 points.

![image](https://github.com/user-attachments/assets/4fde7824-b62a-478a-921c-d41965f8740d)

These results allows stats analytics determine who are top scorers in the league, this helps with individual player rankings.

2. Query 2 gives us the total games the lions have won.

![image](https://github.com/user-attachments/assets/d6905097-dee4-428a-ac0f-4165e0374b1c)

This query can be useful to filter down the games where the lions have performed well as well as seeing how many points were scored and allowed.

3. Query 3 gives us the name of a coach, name of their team, and their sart and end date for the team they coached for with the restictions being they coached for more than 10 years and have at least 2 champ wins.

![image](https://github.com/user-attachments/assets/274b266f-f11e-4533-9a8a-07cdee96f7b8)

This query gives us the best, most experienced coaches in the league.

4. Query 4 gives us player name and jersey number of players whos position are Forward as well as being injured.

![image](https://github.com/user-attachments/assets/72a5ef54-22c1-408f-9586-852ac21bbb0f)

This query is useful for that it gives us players that may have an injury in the near future, since those who have been injured in the past are more likly to have problems later on.

5. Query 5 givs us the first and last name of players, when they were transferred and to what team they went to.

![image](https://github.com/user-attachments/assets/ac0e9bf8-d63d-45d5-a18f-33e0346d4873)

This query grants us insight of where and when players are getting tranferred, since contracts are private we can only make inferences on what happens behind the scenes.

6. Query 6 selects players first and last name, team, location, and calculates a point ratio and is then ordered by this ratio.

![image](https://github.com/user-attachments/assets/346ffe85-867d-4915-8031-51054be72ecb)

This query calculates the total points scored by the team and divides it by the amount of points scored by the player. This shows us how much of the points scored in a game is scored by the player.

7. Query 7 gives us every player from the USA who recived an MVP award.

![image](https://github.com/user-attachments/assets/b5ce974b-cbbe-4660-811f-00b09797ae7c)

We can see what american players get MVP awards.

8. Query 8 gives us the team, city, total points scored by the team, and the average hight of the team players but only those whith 5 or more years experience.

![image](https://github.com/user-attachments/assets/ac340fc0-c7a0-4fcc-a094-ebed85993a38)

This can show us how much height influences points scored, and if teams with taller players do better on average.







