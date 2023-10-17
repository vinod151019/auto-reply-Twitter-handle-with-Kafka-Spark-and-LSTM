# auto-reply-Twitter-handle-with-Kafka-Spark-and-LSTM
Aim:  This project automatically replies to query-related tweets with a trackable ticket ID generated based on the query category predicted using deep learning models. The whole process is automated with tweepy API and Big Data techniques with final deployment on AWS.

Business Overview:

At the heart of artificial intelligence (AI) lies natural language processing (NLP), an innovative field that empowers computers to decipher text and spoken words just like humans. NLP plays a crucial role in various tasks that enhance computer comprehension through structured language interpretation.

One fascinating application of NLP is social media sentiment analysis, which uncovers hidden insights from various social media platforms. As an invaluable commercial asset, NLP assists companies in extracting attitudinal and emotional reactions to products, promotions, and events through language analysis in posts, comments, and reviews. This valuable information can be harnessed for product development, customer service enhancement, and accurate advertising campaigns. By incorporating named entity recognition (NER) techniques, businesses can detect meaningful words and sentences within data. The entire process can be streamlined, automated, and deployed on the cloud by integrating data ingestion and distributed processing services.

Our Twitter Support project aims to monitor live tweets containing specific tags and broadcast them to a Kafka topic, subsequently utilizing Spark Stream to consume the data. After undergoing NLP-driven refinement within a processing pipeline, the tweets will be systematically categorized based on sentiment and query type through advanced machine learning models like LSTM. Finally, using Flask and Tweepy API, each tweet will receive a personalized response featuring a custom ticket ID.

Data Description:

For the training purposes in this project, we have used an “airline tweets” dataset, which includes necessary fields like airline names as tags, actual text, sentiment class, i.e., positive, negative, or neutral and a topic class which can be one of these:

Baggage Issue
Customer Experience 
Delay and Customer Service
Extra Charges
Online Booking
Reschedule and Refund
Reservation Issue
Seating Preferences
Tech Stack:

➔ Language: Python3

➔ Services: Confluent Kafka, Spark

➔ Libraries: tweepy, Flask, kafka, spacy, sklearn, keras, numpy, pyspark, nltk, matplotlib, os

Tweepy for fetching tweets and replying.
Flask for setting up API for a reply.
Kafka for data ingestion.
Sklearn for model evaluation and encoding.
Nltk for preprocessing.
Spacy for named entity recognition.
Pandas for data manipulation and analysis.
Matplotlib for plotting graphs.
Numpy for array and math operations.
Tensorflow and Keras for loading and building models and Embeddings.
Pyspark for UDFs and Streaming.
Os for operating folders.
Approach :

Dataset is first processed by removing Stopwords, mentions, URLs, etc., and Lemmatization.
Tokenizing and Embedding words to text sequences.
 A sequential model is trained on the processed data, which includes LSTM for Sentiment Classification.
Topic labelling using Latent Dirichlet Allocation (LDA).
Data is trained on a sequential model including LSTM for Topic Classification.
Named Entity Extraction.
Saving all models and embeddings for runtime usage.
Sink enriched data to a parquet file.
Reply to the tweet using Flask and tweepy.

