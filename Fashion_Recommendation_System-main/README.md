# Fashion_Recommendation_System

# Objective
Our project aims to learn and implement Deep Learning CNN Architecture as well as Image Processing. We have decided to build a Fashion Recommendation system which provides five similar images with respect to the given input image. We will build our model instead of using a Pre-Trained model like Resnet50, or VG16.   
To handle the response time we will convert our images into vectors and extract their features. later on, we save the model and extracted features to reduce processing time and add the features of our input image to the dataset. After calculating similarity scores we provide recommendations.

# Libraries

Tensorflow  
Numpy  
Pandas  
Matplotlib  
Seaborn  
CV2  
Scikit-Learn  
Pickle  

# Workflow 

* Load the dataset and perform EDA. After exploring, visualize the dataset using Matplotlib and Seaborn
  
* Start building the CNN Model. It has 3 convolution, 3 pooling layers, one flatten layer, 2 dense layers and a dropout of 0.5 for optimization

* Model is complied and optimized using Adam with a learning rate of 0.001

* Before extracting the features we resize the image using CV2 according to the size set in our model

* Then we calculate the cosine similarity of all the images stored in the dataset and save the normalized features in a numpy file

* After that we extract the features of our input image as well and combine it with the dataset providing recommendation

* We save the model as a pickle file so we don't have to repeat the process over and over again hence, saving time

* We load the pickle file and calculate similarity again but this time we also calculate the similarity scores of our resulting five images for evaluation


  # Observations & Future scope

* While exploring we found women had the largest share in types of clothing while clothes for respective seasons had an almost similar share

* The dataset contains fashion items which belong to the time period of 2010-18 with the majority of items from the year 2012
 
* Building our own CNN model was a challenge and while building we experimented with dropout and learning rates which produced different outputs. The best solution came with a learning rate of 0.001
 
* To reduce the processing time we converted the images into vectors and stored them in numpy file which reduced our output time by 70%
 
* For future scope, evaluation by similarity score won't be enough so it will be better to compare our model results with a pre-trained model
