# Machine-Deep-Learning-Combination-Fake-News-Detection
A machine learning and deep learning program to detect fake news from the training and testing datasets provided by Kaggle. The repository contains two .ipynb Google Colab notebooks and .py scripts(in case local execution is preferred). Also datasets for training and testing are provided in the repository.

# Machine Learning used in Fake News Detections:
The program uses an Unprunned DecisionTreeClassifier from scikit-learn library to detect fake news from the kaggle dataset.
The program was evaluated based on accuracy scores of 3 algorithms. The algorithms applied were:

1. GaussianNB
2. DecisionTreeClassifier
3. Support Vector Machines(SVM)

Out of above 3 algorithms, DecisionTreeClassifier provided an accuracy score of 88%.

DecisionTreeClassifier(DCT) - Prunned and Unprunned
1. Prunned DCT provided accuracy of 51% due to entropy and depth constraints
2. Unprunned DCT provided accuracy of 88% and the visualized DCT is also included in this project repository.

# Deep Learning used in Fake News Detections:
The program uses the Sequential 1-Dimensional Convolutional Neural Network from Keras of Google's Tensorflow Library.
The neural network contains below given layer specifics(layers in the network are used in same order as specified below):

1. Embedding Layer as 20800 input dimensions - First Layer(The Input Layer)
2. First Dropout Layer to regularize the network's input layer output.
3. The 1D Convolutional Layer with 250 filters of kernel size 3 - S Layer.
4. A 1D GlobalMaxPooling Layer to Max Pool the Convolutional Layer's output i.e. calculating maximums in each patch of the Convolutional Layer outputs.
5. A Vanilla Hidden Layer with 'relu'(Rectified Linear Unit) activation function.
6. Second Dropout Layer to regularize the network's Vanilla layer output.
7. Final Output Layer with 'sigmoid' activation function.

The above layer specifications can be verified by executing following command in Python Shell:
      model.summary()
      
Since the datasets contain bulk of categorical data, the encoding technique and decoding technique of data is not conventional. The scripts contains some cell with commands that are supposed to be executed only once. Multiple executions of that cells may lead to data corruption and one has to start again from read_csv() step.

# The Python Notebooks were created and executed on Google Colaboratory
It is best advised to use the python notebooks in google colab to achieve best results.

# Some Important and Useful Links:
Kaggle -Fake-News- Dataset Link: https://www.kaggle.com/c/fake-news/data
Tensorflow Keras Link: http://keras.io/
Scikit-learn Link: https://scikit-learn.org/

In case of any suggestions, corrections and contributions kindly drop a mail at husain.amreliwala52@gmail.com

- Happy Machine and Deep Learning!!
