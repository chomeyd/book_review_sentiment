# Books Review Sentiment
## Purpose
The purpose of this project is to implement recurrent neural networks in Keras to 
try and ​classify book reviews as either positive or negative.

## Preprocessing the Data
In order to feed this data into our network, all input reviews must have the same
length. Since the reviews differ heavily in terms of lengths, we either need to trim
or pad the reviews so that they are the same length. For this task, we set the
length of reviews to the mean length, which is around 4 words. If reviews are
shorter than 4 words we need to pad them with zeros, if they are longer than 4
words we trim them to this length by cutting off any words after this. 


##  BUILDING THE MODEL

The network will  has the following  layers;
1.	Embedding layer
2.	SpatialDropout1D(0.2)
3.	BatchNormalization()
4.	LSTM(32)
5.	Dense(2, activation='softmax')

## TRAINING THE MODEL AND MAKING PREDICTION

​The model is them compiled and trained on the test data. The hyperparameter output_dim
in the embedded layer is set for different values, 10 25 50 and 100 to see how different models
perform. the value 50 seemed to have performed better in terms of accuracy. this model was then used to predict 
data