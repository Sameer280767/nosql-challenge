# UK Food Standards Agency Data Analysis

The UK Food Standards Agency evaluates various food establishments across the United Kingdom and assigns them food hygiene ratings. This project involves working with the data from the Food Standards Agency to help the editors of the food magazine "Eat Safe, Love" evaluate and analyze the ratings data for future articles.

## Part 1: Database and Jupyter Notebook Set Up
In part 1, we load the json file as a database and estblish te MongoDB has one collection called `establishments`

## Part 2: Update the Database
In Part 2, we make various modifications to the database as follows
1. Data for a new restaurant is added and inserted into the collection
2. We then find BusinessType for "Restaurant/Cafe/Canteen" (as Penang is the same type) and read in BusinessTypeID for these class of restaurants
3. This is done as BusinessTypeID for Penang is blank and the id is then added
4. We then delete all documents where LocalAuthorityName is "Dover" and confirm the deletion has taken effect in the collection (establishments)
5. Lastly latitude/ longitude data which is stored as string is converted to decimal and RatingValue field is converted to an integer

## Part 3: Exploratory Analysis
In Part 3, we explore the database to answer specific questions from the magazine editors. We use the Jupyter Notebook named NoSQL_analysis_starter.ipynb for this analysis.
We write queries to answer the following 4 questions

#Question 1. What is the number of documents in collection: establishments having Hygiene score equal to 20?
#Answer 1. 41 documents

#Question 2. Which establishments in London have a RatingValue greater than or equal to 4?
#Answer 2. 33

#Question 3. What are the top 5 establishments with a RatingValue rating value of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
#Answer 3. Nearest is defined as within 0.01 degree on either side of the latitude and longitude. These are
   'BusinessName': 'Volunteer'
   'BusinessName': 'Plumstead Manor Nursery'
   'BusinessName': 'Atlantic Fish Bar'
   'BusinessName': 'Iceland'
   'BusinessName': 'Howe and Co Fish and Chips - Van 17'

#Question 4. How many establishments in each Local Authority area have a hygiene score of 0?
#Answer 4. There are 55 documents where hygiene scores are zero sorted in descending order and grouped by LocalAuthorityName
   

