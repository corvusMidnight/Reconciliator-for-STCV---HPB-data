# Reconciliator for STCV-HPB data

The following program is built to reconcile data from an sqlite STVC database with data from the online HPB database.
The sqlite database can be downloaded from the following [GitHub repository](https://github.com/TomDeneire/InformationScience/tree/main/course/data).



The program takes an squilte3 connection and performs a query of 100 book titles from an stcv database and collects title, author, and yop inside a dictionary
Through a HPB’s SRU/CQL query, it  executes two queries:

- If author, title, and year of publication are available inside the stcv database, uses all of them to return the first 10 matches
- If some of the values are missing, queries only by title

It does not return an object: it prints out the matches for each c:stcv with HPB, who the author is for that record. what's the year of publication,
#and compares them to the searched author and yop

**Note**: there is not comparison for title search: this comparison is available only for the second query. No titles were matching
          due to the diffences in spelling

**Note**: U have bettered the code to include author and yop for each record in the first query to asses the quality of match
          for each match. This causes 14 records to not be match. If that part of the code is erased, the code will match all
          the records. Between a program that returns 84 matches with additional info about the match quality and one that returns
          100 matches with no information about any of those matches, I have chosen the former.


![alt text](https://cdn.aarp.net/content/dam/aarp/entertainment/books/2021/12/1140-flying-books-illustration.jpg)
