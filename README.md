# CSE508_Winter2023_A2_14

## Assignment info

Course: Information Retrieval [CSE508]
Semester: Winter 2023
Group: 14
Assignment 2


## Repository Description

A2_Q1.ipynb: Complete code with comments for Question 1
Q2.ipynb: Complete code with comments for Question 2 
A2_Q3.ipynb: Complete code with comments for Question 3


## .gitignore Description

All the data files are stored in the Dataset folder which is present in the root folder. Link to pkl files : https://drive.google.com/drive/folders/1SvywomEWwR28FZTLpJX3nZLHu5NpI95J 


* Question 1

 *Methodology (Q1a. TF-IDF matrix)
    *Relevant libraries are imported
    *List of path of all the files in the dataset is determined and a file_dictionary is constructed
    *Each document is preprocessed as done in Assignment 1
    *Global vocabulary is created
    *matrix of size no. of document x vocab size is constructed
    *above matrix is filled with TF-IDF values
    *Query is input and sanitized with the same preprocessing steps
    *The query vector is made of size of vocabulary
    *TF-IDF score of query is computed using TF-IDF matrix
    *Top 5 documents based on above score are displayed
    *Same is repeated for all 5 weighing schemes
    
 *Methodology (Q1b. Jaccard Coefficient)
    *Relevant libraries are imported
    *List of path of all the files in the dataset is determined
    *Each document is preprocessed as done in Assignment 1
    *Query is input and sanitized with the same preprocessing steps
    *Jaccard Coefficient for doc,query pairs is found
    *Top 5 relevant documents based on jaccard coefficient are displayed
    
    
* Question 3

  *Methodology
    *Relevant libraries are imported
    *List of path of all the file in the dataset is determined
    *Qid:4 is extracted and stored in a separate list and rest all the rows are stored in another list
    *The list is sorted in descending order
    *Total number of files is calculated
    *nDCG at 50 and whole dataset is calculated
    *Precision-Recall graph is plotted on feature 75
