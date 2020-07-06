# Movies-ETL


Adding try-except blocks will make the automated ETL script more robust to errors.

1.
The "def insert_or_create" was added based on the asumtion that sometimes there is new data for a table that does not exist.

2.
The      "try:
                   print('connection closed')
                   self.cursor.close()
                   self.conn.close()
              except:
                   print('error closing connection')
                   assume error in connection."      was added based on the assumtion that some new data could not be connecting well and thus would stop the flow without warning. So the Print error message was created to alert the user. 
 
3.
Based off of the assumption that there are different or missing title names in kaggle or wikipedia the line "movies_df[(movies_df['title_kaggle'] == '') | (movies_df['title_kaggle'].isnull())]" was added to make differences clear. 

4. 
Based off the assumption that kaggle had some missing data the line "def fill_missing_kaggle_data(df, kaggle_column, wiki_column)" was created so that wikipedia could fill in the missing data from the same movies. 
