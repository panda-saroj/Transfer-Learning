# Transfer-Learning
Transfer Learning applied to MNIST dataset

Transfer learning is a machine learning method where learnings from a model developed for a task is reused 
as the starting point for a model on a second related task. 
In most practical use, the initial trained layers of the trained model are transferred to the new model 
and new layers are added on top of those to handle the problems of the second task. 

The code performs transfer learning on the MNIST dataset.
Trains a first model using the digits [0,1 …6]. This model has two parts.
feature_layers consisting of several convolution layers to extract the feature maps from the digit images.
classification_layers consisting of a few Dense Fully connected layers with the last layer having softmax activation function 
to classify the images.

After the first model is trained, a second model is built using the trained feature_layers of the first model and 
adding a few dense layers on top of those trained layers to classify the digits [7,8,9]. 
The training for the trained convolution layers was turned off, which results in significant improvement in the training time without 
loosing accuracy in the classification task. 
The results from the experiment are given below. 
In both the results, test accuracy is more than 99%. 
Each model was trained for 10 epochs. 

Train on 41935 samples
Epoch 1/10
41935/41935 [==============================] - 81s 2ms/sample - loss: 0.1591 - accuracy: 0.9494
Epoch 2/10
41935/41935 [==============================] - 80s 2ms/sample - loss: 0.0505 - accuracy: 0.9862
Epoch 3/10
41935/41935 [==============================] - 84s 2ms/sample - loss: 0.0388 - accuracy: 0.9886
Epoch 4/10
41935/41935 [==============================] - 89s 2ms/sample - loss: 0.0299 - accuracy: 0.9917
Epoch 5/10
41935/41935 [==============================] - 83s 2ms/sample - loss: 0.0255 - accuracy: 0.9921
Epoch 6/10
41935/41935 [==============================] - 83s 2ms/sample - loss: 0.0215 - accuracy: 0.9932
Epoch 7/10
41935/41935 [==============================] - 90s 2ms/sample - loss: 0.0200 - accuracy: 0.9938
Epoch 8/10
41935/41935 [==============================] - 93s 2ms/sample - loss: 0.0190 - accuracy: 0.9943
Epoch 9/10
41935/41935 [==============================] - 87s 2ms/sample - loss: 0.0155 - accuracy: 0.9953
Epoch 10/10
41935/41935 [==============================] - 81s 2ms/sample - loss: 0.0157 - accuracy: 0.9952
Training time: 0:14:12.421031
Test Loss: 0.016816775628637613
Test accuracy: 0.99456286
Train on 18065 samples
Epoch 1/10
18065/18065 [==============================] - 11s 631us/sample - loss: 0.0457 - accuracy: 0.9846
Epoch 2/10
18065/18065 [==============================] - 11s 590us/sample - loss: 0.0167 - accuracy: 0.9945
Epoch 3/10
18065/18065 [==============================] - 11s 594us/sample - loss: 0.0114 - accuracy: 0.9963
Epoch 4/10
18065/18065 [==============================] - 10s 571us/sample - loss: 0.0077 - accuracy: 0.9977
Epoch 5/10
18065/18065 [==============================] - 10s 569us/sample - loss: 0.0087 - accuracy: 0.9968
Epoch 6/10
18065/18065 [==============================] - 10s 563us/sample - loss: 0.0062 - accuracy: 0.9977
Epoch 7/10
18065/18065 [==============================] - 10s 562us/sample - loss: 0.0056 - accuracy: 0.9985
Epoch 8/10
18065/18065 [==============================] - 10s 567us/sample - loss: 0.0069 - accuracy: 0.9978
Epoch 9/10
18065/18065 [==============================] - 10s 573us/sample - loss: 0.0060 - accuracy: 0.9977
Epoch 10/10
18065/18065 [==============================] - 10s 568us/sample - loss: 0.0056 - accuracy: 0.9978
Training time: 0:01:44.644059
Test Loss: 0.016776055597074967
Test accuracy: 0.9956825



