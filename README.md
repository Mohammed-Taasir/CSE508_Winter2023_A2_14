# CSE508_Winter2023_A2_14

## Assignment info

- Course: Information Retrieval [CSE508]
- Semester: Winter 2023
- Group: 14
- Assignment 2


## Repository Description

- A2_Q1.ipynb: Complete code with comments for Question 1
- Q2.ipynb: Complete code with comments for Question 2 
- A2_Q3.ipynb: Complete code with comments for Question 3


## .gitignore Description

All the data files are stored in the Dataset folder which is present in the root folder. Link to pkl files : https://drive.google.com/drive/folders/1SvywomEWwR28FZTLpJX3nZLHu5NpI95J 


* Question 1

  * Methodology (Q1a. TF-IDF matrix)
    * Relevant libraries are imported
    * List of path of all the files in the dataset is determined and a file_dictionary is constructed
    * Each document is preprocessed as done in Assignment 1
    * Global vocabulary is created
    * matrix of size no. of document x vocab size is constructed
    * above matrix is filled with TF-IDF values
    * Query is input and sanitized with the same preprocessing steps
    * The query vector is made of size of vocabulary
    * TF-IDF score of query is computed using TF-IDF matrix
    * Top 5 documents based on above score are displayed
    * Same is repeated for all 5 weighing schemes
    
  * Methodology (Q1b. Jaccard Coefficient)
    * Relevant libraries are imported
    * List of path of all the files in the dataset is determined
    * Each document is preprocessed as done in Assignment 1
    * Query is input and sanitized with the same preprocessing steps
    * Jaccard Coefficient for doc,query pairs is found
    * Top 5 relevant documents based on jaccard coefficient are displayed

  * Jaccard Coefficient
     * Pros: Faster and requires less space as we don’t need to make the size of query vector equal to that of document vector
     * Cons: Does not take into account important metrics like term frequency and ordering of words

  * TF-IDF Matrix
     * Pros: Takes into account term frequency of document and query. Terms occurring highly in a small number of documents are given more weightage and less weightage to terms occurring in almost all documents.
     * Cons: Slower and requires more space as we have to make the size of query equal to length of document. Doesn’t take into account position of term in document, semantics and co-occurrences in different documents.


* Question 2

  * How to run the code
  
    1.	First perform EDA.
    2.	Preprocess the data by Lower casing, removing punctuations, numbers, stopwords, perform lemmitization, tokenization.
    3.	The fit function takes in the BBC_data_matrix and train_tf_icf dictionary which contains the tf-icf values for each word in each category in the training data.
    4.	The function then calculates the category_tf_icf for each category, which is the sum of tf-icf values for each word in that category.
    5.	Next, it calculates the probability of each word in each category using the tf-icf values and the catgory_tf_icf values. This is stored in the words_proba dictionary.
    6.	 Finally, it calculates the prior probabilities for each category using the number of articles in each category in the training data. These prior probabilities are stores in the nb_prior_proba dictionary.
    7.	The output of the function is words_proba and nb_prior_proba, which contains the probabilities for each word in each category and prior probabilities for each category.
    8.	The conclusion is that the fit_NBTF_ICF function calculates the probabilities required to apply the Naïve Bayes algorithm using the tf-icf values.
    9.	Posterior probability is calculated for each category of the test documents, by multiplying 
    10.	The prior probability with the probability of each word in the test document given the category, as calculated using the training set.
    11.	The code iterates through each document in the test set and for each document, calculates the posterior probability of it belonging to each category using the Naïve Bayes algorithm with tf-icf weighing. 
    12.	Finally the category with the highest posterior probability is assigned as the predicted category for that document.
    13.	The function predict_documents() takes in three arguments – docs which is a pandas dataframe of the documents to be predicted, nb_pior_proba which is a dictionary of prior probabilities for each category and the words_proba which is a dictionary of the probabilities for each word in each category.
    14.	For each document, the function calculates the posterior probability for each category based on the prior probabilities and the probabilities for each word in each category. Then it predicts the highest probability as the predicted category for that document. It returns a list y_pred which contains the predicted category for that document.
    15.	Based on the predictions, we can evaluate the accuracy of the Naïve Bayes classifier on the test set and compare it with other classification algorithms to determine the best model for this particular text classification problem.

    
    
* Question 3

  * Methodology
  
    * Relevant libraries are imported
    * List of path of all the file in the dataset is determined
    * Qid:4 is extracted and stored in a separate list and rest all the rows are stored in another list
    * The list is sorted in descending order
    * Total number of files is calculated
    * nDCG at 50 and whole dataset is calculated
    * Precision-Recall graph is plotted on feature 75
