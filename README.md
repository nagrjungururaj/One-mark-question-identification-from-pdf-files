# One-mark-question-identification-from-pdf-files
The algorithm identifies all questions corresponding to 1-mark in a question paper
# Dataset
1. The raw data are pdf files / question papers of social studies subject SSLC of KSEEB  
Download from here : http://kseeb.kar.nic.in/sslc_model_qp_2019.asp
2. The raw data consisting of 10 question papers is converted to .csv files using manual annotations of question extraction and labeling. The 'train.csv' and 'test.csv are the corresponding files used in the algorithm

# Approach 
The approach of designing the algorithm can be found in file 'approach.jpg'. The algorithm uses a pre-trained word embedding to convert the sentences / words to vectors which are inputed to LSTM.  
Download the word embedding from here : https://fasttext.cc/docs/en/english-vectors.html

# Run
Just run the notebook predict_question_type.ipynb to visualize the results

# Requirements
Python 3+, pandas, numpy, scikit-learn, keras (with tensorflow backend)

# Results
The algorithm predicts the question sentences correctly for the test question sentences and achieves a F1-score for train data : 98.93 %  

Test evaluation is not possible as the test question sentences do not contain labels. I have purposely not labeled them, due to the nature of the use case. One could label them and calculate the metrics for test data

# Cons
1. Data gathering and labeling is a challenge ! 
2. In this ccurrent approach, there is no suitable method found to extract the questions from raw pdf files ! 

# Improvement
To address the data extraction, I suggest another approach which solves this problem which can be found in 'improved.jpg' which is self explanatory (Note this requires a bit longer time for more data and lebeling, but addresses the data extraction problem)
