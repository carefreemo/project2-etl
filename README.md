# project2-etl
 
Extracting Data
Step 1: Pulled information from Data.world (different users)
o	Top Universities from 2017 (https://data.world/datadavis/nba-salaries)
o	NBA Players ( https://data.world/education/university-rankings-2017) 


Transforming Data
Step 1:  Import libraries

Step 2: Import and read the National University Rankings csv file

Step 3: Use the head function to refer school rankings (we are maininly looking for top 10 unis and to review the data)

Step 4: Use the drop function to drop any university that is not a top 10 school

Step 5: Use the Data Frame function to create a data frame for the new University data set

Step 6: Use the rename function to rename the 'Name' column to 'college'

Step 7: Import and Read the Players csv file 

Step 8: Use the DataFrame function to create a data frame for the Players file

Step 9: Use the dropna function to drop any row that has NAn in the 'college' 

Step 10: Use the str.contains function to find look iny  the 'college' column and replace any cell that contains 'Stanford University' with 'Standford University'

Step 11: Use the str.contains function to find look iny  the 'college' column and replace any cell that contains 'Duke University' with 'Duke University'

Step 12: Use the str.contains function to find look iny  the 'college' column and replace any cell that contains 'University of Pennsylvania' with 'University of Pennsylvania'

Step 13: Use the merge function to perform a right join (PlayersClean (left) and UniversitiesClean (right))




Loading Data
Step 1: Open PostgresSQL (relational database) and created a new database 

Step 2:  Connect to PostgresSQL with engine

Step 3: Created two tables in PostgresSQL


Why NBA Data?

We were curious to create a database that would allow us to know all of the players that were enrolled into a top 10 ranked universities in the US 

This database can also gives us infomation about the players regarding personal history and sport history such as: birth date, position, draft year, draft pick, etc


We wanted to simulate what it was like to gather data the way it would be done in the real world 


Findings: 

We found that no players came from MIT and University of Chicago. 

135 players went to a top 10 university
