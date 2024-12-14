# Finding-Similar-Items

The aim of this project is to find similar pairs or sets of job offers published on Linkedin. The column used to build the similarity detector is job_summary in the job_summary.csv file from the dataset ‘Linkedin Jobs & Skills’ published on Kaggle under the ODC-By license.

The main techniques used are:
- **TF-IDF (Term Frequency-Inverse Document Frequency)**: for each document (job description) the algorithm evaluates the importance of its tokens (words) considering the amount of times they appear within a document with respect to the total and their frequency across all the documents.
- **MinHashing**: used to reduce the dimensionality of the documents by building a MinHash signature for each document.
- **LSH (local sensitivity hashing)**: used to reduce the number of comparisons between items by using hash functions and taking as input the minhash signatures of the documents.

The implementation is made suitable for big datasets by using PySpark. 
