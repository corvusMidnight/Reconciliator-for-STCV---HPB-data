# Reconciliator for STCV-HPB data

The following program is built to reconcile data from a local sqlite STVC database with data from the HPB online.
The sqlite database can be downloaded from the following [GitHub repository](https://github.com/TomDeneire/InformationScience/tree/main/course/data).



The program takes an squilte3 connection and performs a query of 100 book titles from an stcv database collecting title, author, and yop inside a dictionary

Then, through the data collected and HPB’s SRU/CQL, it performs two queries in the HPB databasr:

- If author, title, and year of publication are all available inside the stcv database, uses all of them to return the first 10 matches with their respective identifier
- If some of the values are missing, queries only by title

It does not return an object: it prints out the matches for each c:stcv with HPB, who the author is for that record. what's the year of publication,
#and compares them to the searched author and yop

**Note**: there is not comparison for title search: an approximative comparison is available only for the second query. No titles were identical
      due to the diffences in spelling
      
**Note**: for the reconciliator to work, title must be available

**Note**: I have bettered the code to include author and yop for each record in the first query to asses the quality of match
      for each match. However, the comparison has its limitations: some authors and yop are different just because they
      two catalogues report them in a different manner or because some extra characters are added within the HPB tag
      
#### Code updated to Saturday 29/1/2022  ####

![alt text](https://cdn.aarp.net/content/dam/aarp/entertainment/books/2021/12/1140-flying-books-illustration.jpg)
