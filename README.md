# TensorFlow Binary Image Classification using CNN's
This is a binary image classification project using Convolutional Neural Networks and TensorFlow API (no Keras) on Python 3.
[Read all story in Turkish](https://medium.com/@mubuyuk51/tensorflow-i%CC%87le-i%CC%87kili-binary-resim-s%C4%B1n%C4%B1fland%C4%B1rma-69b15085f92c).
# Dependencies

```pip install -r requirements.txt```

or

```pip3 install -r requirements.txt```

# Training
```python tensorflow_binary_image_classification1.py ```

or change directory and run on Terminal:

```jupyter lab ``` or ```jupyter notebook ```

# Data
This is a repository containing datasets of 6400 training images and 1243 testing images.No problematic image.

Download dataset from [here](
https://www.dropbox.com/s/ezmsiz0p364shxz/datasets.rar?dl=0). It is 101 MB.

Extract files from datasets.rar. Then put it in TensorFlow-Image-Classification-Convolutional-Neural-Networks folder.
train_data_bi.npy is containing 6400 training photos with labels.

test_data_bi.npy is containing 1243 testing photos with labels.

Classes are table & glass.

Classes are equal(3200 glass - 3200 table). 

# CPU or GPU
I trained on GTX 1050. 1 epoch lasted 3-4 minutes approximately.

If you are using CPU, which I do not recommend, change the lines below:
```
config = tf.ConfigProto(allow_soft_placement=True)
config.gpu_options.allow_growth = True
config.gpu_options.allocator_type = 'BFC'
with tf.Session(config=config) as sess:
```
to
```
with tf.Session() as sess
```
# Architecture

1 input layer, 4 convolution layer, 4 pooling layer, 2 fully connected layer, 2 dropout layer, 1 output layer. The architecture used is below.

![alt text](https://github.com/MuhammedBuyukkinaci/TensorFlow-Image-Classification-Convolutional-Neural-Networks/blob/master/MY_ARCHITECTURE.png) 

# Results
Accuracy score reached 90 percent on CV after 50 epochs.

![alt text](https://github.com/MuhammedBuyukkinaci/TensorFlow-Image-Classification-Convolutional-Neural-Networks/blob/master/accuracy.png)

Cross entropy loss is plotted below.

![alt text](https://github.com/MuhammedBuyukkinaci/TensorFlow-Image-Classification-Convolutional-Neural-Networks/blob/master/loss.png)

