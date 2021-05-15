# Election Analysis with Python

## Overview of Election Audit

Tom, a Colorado Board of Elections employee, is auditing the election results for the U.S. Congressional precinct in Colorado. Tom assigned me to generate a vote count report to certify this U.S. congressional race which needs to include following results:
  - The total number of votes cast
  - The voter turnout for each county
  - The percentage of votes from each county out of the total count
  - The county with the highest turnout
  - The total number of votes for each candidate
  - The percentage of votes for each candidate
  - The winner of the election based on the popular vote

Furthermore, Tom's manager wants Tom and me to write a code to automate the election audit process using Python. This code will be used to audit not only other congressional districts but also senatorial distrcits and local elections.

## Election-Audit Results

### Results on County
![County_Votes_and_Percentage](https://user-images.githubusercontent.com/82549782/118345335-9be4f400-b501-11eb-9147-04804b19917e.png)

- 369,711 votes were cast in this congressional election.
- The voter turnout and the percentage of votes for each county are:
  - Arapahoe has 24,801 votes in total, the turnout rate is 6.7%.
  - Denver has 306,055 votes in total, the turnout rate is 82.8%.
  - Jefferson has 38,855 votes in total, the turnout rate is 10.5%.
- According the information above, the county with the highest turnout rate is **Denver**.

### Results on Candidate
![candidate_votes_and _percentage](https://user-images.githubusercontent.com/82549782/118345475-aa7fdb00-b502-11eb-8c48-d3a521878fc3.png)

- The total number of votes and percentage of votes for each candidate:
  - Raymon Anthony Doane got 11,606 votes which are 3.1% of the total votes.
  - Diana DeGette got 272,892 votes which are 73.8% of the total votes.
  - Charles Casper Stockham got 85,213 votes which are 23.0% of the total votes.
- According the information above, **Diana Degette** won the election.

## Election-Audit Summary

In order to make this script can be used for any election, some modifications should be made according to different datasets. For example:

1. ![modification_row](https://user-images.githubusercontent.com/82549782/118348068-ba54ea80-b515-11eb-90e5-b2fa0d8cb6ed.png)
   - The path to load a file should be changed according to the location where you save the file. The script uses the "join()" function, which can joins file path components together when they are provided as separate strings; it then returns a direct path with the appropriate operating system separator. Therefore, we can add the folder and the file to join together. The folder and file names are modified according to the data file name provided and the folder name in which it is located
   - We can also use direct path in the script, the code would be "file_to_load = 'Resources/election_results.csv'" in this case. The folder and file names can be modified. Furthermore, if the data file is in the same level as python file, then the path would be 'election_results.csv'.

2. ![modification_1](https://user-images.githubusercontent.com/82549782/118347064-54b13000-b50e-11eb-950e-3a9c7e37da99.png)
 
   - As shown in the graph, The candidate name is extracted from the third column of each row, and the county name is extracted from the second column of each row. 
   - To extract the right data, we need to change the row number based on the provided dataset. Since the first column is 0, the number of columns from which to retrieve data should minus one.
