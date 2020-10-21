# Movies-ETL

1.
Kaggle had some missing data the line "def fill_missing_kaggle_data(df, kaggle_column, wiki_column)" was created so that wikipedia could fill in the missing data from the same movies.Assumption is data is clean, but if it isn't the functipn will clean it for us. When cleaning out the movie data file, we included some key values to try and find alternative titles. We need to assume that we listed out all the key values and alternative titles. If we did not get all of the key values then our data would be need more cleaning. Key values were used to find alternative movie titles - it can be assumed all key valyes and alternative titles were listed - if not, data would need more cleaning.

2.
The "def insert_or_create" was added based on the asumtion that sometimes there is new data for a table that does not exist. 

3.
We can assume that both of the CSV's have a column that is named "imdb_id" This explains why we inserted the try-except in the event any csv doesn't have the "imdb_id" column.Adding try-except blocks will make the automated ETL script more robust to errors.

4.   
Function can only work if user running it has all files called out





