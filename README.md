# NYC-Taxi-Limousine-Commission-Project
This contains all the files associated with this project and analysis

## Table of content
* Project Description
* Project Objectives
* Data Gathering
* Data transformation
* Data modelling
* Data and report limitation
* Conclusion
* Recommendation


-----------

# Project Description


This dataset was provided to be worked on as a group project. The unanalysed dataset contained close to 1.7 Million rows. The analysis was performed using Microsoft PowerBI because the dataset was too large for Microsoft Excel to handle. It also contained some guidelines to follow when doing the cleaning. Important to say, the dataset contained a data dictionary to explain some terms in the main NYC Trips data, the main NYC trips data, a fiscal calendar and Topo Json file showing the maps of new york.

--------
# Project Objectives

    This project was to provide insights to some following questions
    
* What's the average number of trips we can expect this week? 
* What's the average fare per trip we expect to collect? 
* The average distance travelled per trip?
* How do we expect trip volume to change, relative to last week? 
* Which days of the week and times of the day will be busiest? 
* What will likely be the most popular pick-up and drop-off locations?

-------
# Data Gathering
This dataset has been gathered by the New york city taxi and limousine commission for over four years.



-------
# Data transformation

    I loaded everything as related to the project
    Then I duplicated our original Data
    Created a table for all the necessary columns because my visuals needed something to rep with.
    I also made sure the Pick up dates were before the drop off dates and it was consistent throughout the roles.
    I then did subtraction between the pick up date and  drop off date in order to discover the outliers and filter those that had a difference of more than 1 days as the cleaning guideline stated.
    I also filtered out dates that were before 2017 and after 2020
    I then filtered out rows that had both a fare amount and trip distance of 0 using advanced filtering
    I then replaced the passenger count that had fields equals to "Null" and "Zero" with "One"
    After all the past steps, I then added ID to the data as there was no other filtering to do again. Renamed it as trip ID
    Then converted all the remaining columns to their appropriate data types
    I also splitted columns that had both date and time format together.
    At this point, I was already done with power query. So I continued the rest of the cleaning in the PowerBi Desktop.
    The remaining filtering was done via the filters pane.
    Then I converted columns in which their fields was negative to positive using DAX.
    I then used some DAX measures to provide insights to some of the questions.



--------
# Data modelling
I adopted the use of a star schema. Creating a representation of all the columns in the facts table and joining them together.
![image](https://user-images.githubusercontent.com/85373417/192124377-456185b6-3b69-4344-97b9-63dca95cedaa.png)



---------
# Data and report limitation
I was not able to provide insight to 2 out of the 6 questions as far as my knowledge in PowerBi is concerned. I also couldn’t make use of map visuals in my dashboard because I don’t understand how to extract Json. There was also some blanks in the data in some columns.

-----------
# Dashboard 
Interact with my project through https://app.powerbi.com/view?r=eyJrIjoiYjAwMzM0NjYtNTA3NC00NTVmLTlkMTUtNzNhYTc0ZTI0M2VjIiwidCI6ImQ3NWRlYTkyLTk2MjktNGZmYi05ZGExLTVmNjcyMTBiNjM1ZCJ9

![image](https://user-images.githubusercontent.com/85373417/194973662-80d0bf7d-2355-4d0f-bb5f-df9370b18198.png)





-------------
# Conclusion
I was able to learn and implement all what i have learnt so far in my learning journey into this project. Implemented the use of Measures, calculated fields, grouping, drillthrough, slicers etc
