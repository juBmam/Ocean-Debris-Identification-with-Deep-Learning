# Metis-Project-5

Metis Project 5: Identifying Underwater Trash Using Neural Networks and Natural Language Processing
By Julian Cheng

In this project, I used images obtained from a conservation database to perform convolutional neural 
network modeling and natural language processing to classify images as either underwater organisms 
or as trash, as well as develop a predictive system that can identify the most commonly encountered
objects underwater. 

Images were standardized by color and size, and run through a convolutional neural
network. The performance was evaluated using the sparse categorical cross entropy function, and 
accuracy using sparse categorical accuracy. 

Classification metrics came out to:
Accuracy: 0.969
Precision: 0.963
Recall: 0.998
F1 Score: 0.980

My curiosity lead me to believe that, if it was possible to predict the most commonly encountered 
objects, adequately preparing autonomous cleaning robots with the right tools could streamline their 
development costs, efficiency, and increase the amount of trash recovered.

Using Mobilenet’s existing neural network as a basis for transfer learning, I applied the predictor 
on the image dataset, split into trash and organisms by label. The predictor would return 5 of the 
most probable classifications for the image. I appended the classifications into a “sentence” and 
repeated the process across the entire dataset to create a corpus. Using TFIDF and an NMF pipeline, 
I was able to identify the most prevalent groupings.

To run this project, unzip the image files and move the contents of the folders into three new folders 
named: train_jpg, val_jpg, test_jpg

Tools used: Keras Convolutional Neural Network, OpenCV, MobileNet Image Recognition, Transfer Learning,
SKLearn, Natural Lancuage Processing, TFIDF, NMF
