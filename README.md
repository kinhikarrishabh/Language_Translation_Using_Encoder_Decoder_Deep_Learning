# Language_Translation_Using_Encoder_Decoder_Deep_Learning
This project works on translating text from Hindi to English using the Encoder Decoder approach of Deep Learning.

# About the Dataset
The name of the dataset we are using is “IIT Bombay English-Hindi Translation Dataset ''. It contains 1,561,840 instances of Hindi-English Translation. 
To facilitate the process of machine translation from English (the source language) to Hindi (the target language), we have adopted an Encoder-Decoder approach. 

# Data Visualization
We have undertaken a series of data visualization techniques. These techniques encompass the creation of a word cloud, which serves as a visual representation to glean insights into the most frequently occurring words within the source and target language datasets. 
Furthermore, we have conducted an in-depth analysis of word counts in both the source and target languages, unravelling the statistical nuances that underlie the language patterns within our data. We have also ventured into the exploration of bigrams, as they hold substantial importance in contributing to the refinement of our translation models. 

# Data Pre-Processing and Model Building
Data Preprocessing, in the cleaning of the data we are following various steps. 
Lowercasing of data, removing quotes, punctuations , digits, add start and end tokens. We will be using the sentences having the length less than 20. 

After performing the above mentioned Data Preprocessing steps we move on the data preparation and splitting stage. We split the data set into training and testing states. 
While training the data, we want to train the model using batches of data and not feed in the entire data. 
For this we introduce a generator function, which generates batches of training data for sequence to sequence models. 

# Model Description
The model used for training is LSTM which stands for Long Short Term Memory. 
We train our model using LSTM, utilizing it's functionality to be able to deal with sequential data. In the last layer, we apply the softmax activation layer so as to get the word/token with the most probability. After the training of the model is complete we decode input sequence using the trained model.

# Result Analysis
X axis shows the epoch and the y axis shows the accuracy. The graph infers that the training accuracy of the model increases at first and then plateaus around 0.95. This means that the model is learning the training data well. The model's accuracy on test data increases over time but doesn't plateau as quickly. Hence we can say that the model is generalizing well.

The training accuracy and testing accuracy diverge around 15 epochs. This is an indication of a model overfitting the data. 
The model reaches its peak performance on the test data at around 20 epochs. Even though the training accuracy is increasing, the model's performance is not improving on the test data.


<img width="435" alt="image" src="https://github.com/kinhikarrishabh/Language_Translation_Using_Encoder_Decoder_Deep_Learning/assets/76053092/0b9acc59-7433-4ab1-8984-1e7cd7e7787c">
