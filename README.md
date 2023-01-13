# project2-etl
 
EXTRACTING DATA

Step 1: Pulled information from Data.world (different users)
o	Top Universities from 2017 (https://data.world/datadavis/nba-salaries)
o	NBA Players ( https://data.world/education/university-rankings-2017) 


TRANSFORMING DATA

Step 1:  Import libraries 

Step 2: Import and read the National University Rankings csv file 

Step 3: Use the head function to refer univeristy rankings (we are maininly looking for top 10 unis and to review the data)

Step 4: Use the drop function to drop any row containing university that is not a top 10 university

Step 5: Use the Data Frame function to create a data frame for csv file

Step 6: Use the rename function to rename the column headers and get rid of any formatting that could cause an error

Step 7: Import and Read the Players csv file 

Step 8: Use the DataFrame function to create a data frame for the Players csv file

Step 9: Use the dropna function to drop any row that has NAn in the 'college' column

Step 10: Use the str.contains function to parse 'college' column and replace any cell that contains 'Stanford University' (due to multiple universities per cell due to transfers, etc) with 'Standford University'

Step 11: Use the str.contains function to parse 'college' column and replace any cell that contains 'Duke University' (due to multiple universities per cell due to transfers, etc) with 'Duke University' 

Step 12: Use the str.contains function to parse 'college' column and replace any cell that contains 'University of Pennsylvania' (due to multiple universities per cell due to transfers, etc) with 'University of Pennsylvania'

Step 13: Use the merge function to perform a right join (PlayersClean (left) and UniversitiesClean (right)). Potential final queriable dataframe or SQL table.



LOADING DATA

Step 1: Open PostgresSQL (relational database) and create a new database called NBA_DB

Step 2: Connect to PostgresSQL with engine in pandas 

Step 3: se the to_sql function to create two tables in PostgresSQL (these 2 tables were transofrmed and cleaned using pandas)

Step 4: Go to properties of each table and assign Primary Keys. In thise case Primary Key in PlayersTable = "_id" and in UniversitiesTable = "college"


WHY NBA DATA?

We were curious to create a database that would allow us to know all of the NBA players that were enrolled into a top 10 ranked university in the US.

This database can also gives us infomation about the players regarding personal history and sport history such as: birth date, position, draft year, draft pick, shoots (right handed or left handed), weight, etc.

Once the database is created we can filter other useful information by year, college name, player name, draft year, postion, etc.


The purpose was to simulate what it was like to extract data the way it would be done in the real world with all its complication, transform it to suit our needs and reduce possibility of error, and finally load wherever we want.


FINDINGS: 

We found that NO NBA player attended MIT or University of Chicago or Johns Hopkins University	

128 NBA players went to a top 10 university

There were only 2 players with the same name in the players dataframe
