# Notes on Data Preparation for ML Training
## Neural Network (NN), Convolutional Neural Network (CNN), and Long Short-Term Memory (LSTM) Models
1. If you are using train_test_split on a csv-format dataset, use '**stratify=y**' to get the same proportion of classes for training and test sets.
2. If your dataset is **binary**, you can utilize 0/1 lables as available in the training set. Accordingly, you have to use **1 unit** for the last FC layer with **sigmoid** activation function. If your dataset is **Multi-Class** with labels as 0/1/2/..., you have to use **tf.keras.utils.to_categorical (train_labels/test_labels)** to get the one-hot-encodings and then use **N (Number of Classes) units** with **SoftMax** activation function in the last FC layer. 
3. If you are classifying images (binary and multi-class) and creating the training and test sets using **flow_from_directory**, use can just pass the information to the model and train it without any need to use one-hot encoding. 
4. If the class labels are not represented in 0/1/2/... format, you can use **from sklearn.preprocessing import LabelEncoder** to get the labels and train the models according to the above instructions. 

## Machine Learning (ML) Models
For ML, you can just pass the classes to the models and get the results without any need to get the one-hot encodings. If the class labels are not represented in 0/1/2/... format, you can use **from sklearn.preprocessing import LabelEncoder** to get the labels and train the models accordingly. 
