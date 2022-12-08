# Classification using SVC & CNN

## Project description
This project is a mini project for the course D7041E at LTU during winter 2022. The project was created by Anton L, Birger W & Joakim VL.

## What is included in the project
The project consists of two [Jupyter Notebooks](https://jupyter.org/) files. 

One of the files, *CNN.ipyn*, includes an implementation of a CNN ([Convolutional Neural Network](https://en.wikipedia.org/wiki/Convolutional_neural_network))

The other file, *SVC.ipyn*, includes an implementation of a SVC ([Support Vector Machine for classification](https://en.wikipedia.org/wiki/Support_vector_machine))

### How to run CNN.ipyn
Simply run `run_multiple_times(_runs=1, _amount_of_data=50000, _epochs=10)` with your wanted parameters. This automatically runs an 80/20 split of the dataset. This line of code is found in the bottom of the file.

Run the code with even numbers for the amount of data. Maximum amount of data possible: 50000. Maximum testdata: 10000.

### How to run SVC.ipyn
Simply run `run_multiple_times(_runs=1, _amount_of_data=500, _use_optimization=True)`with your wanted parameters. This automatically runs an 80/20 split of the dataset. This line of code is found in the bottom of the file.

Run the code with even numbers for the amount of data. Maximum amount of data possible: 50000. Maximum testdata: 10000. Minimum data: 130.


## Requirements & Versions

 - Python: 3.10
 - Tensorflow: 2.9.2
 - Matplotlib: 3.6.2
 - Opencv-python: 4.6.0.66

## Data sets
Cifar 10 dataset from Keras: https://keras.io/api/datasets/cifar10/

The dataset consists of 50,000 32x32 color training images and 10,000 test images split into 10 classes.

The dataset contains the classes:
|Label  |Description  |
|--|--|
| 0 | airplane |
| 1 | automobile |
| 2 | bird |
| 3 | cat |
| 4 | deer |
| 5 | dog |
| 6 | frog |
| 7 | horse |
| 8 | ship |
| 9 | truck |


*This dataset is imported in the python code and will automatically be downloaded once the complete notebook is ran.*

## Recommended testing

### CNN
Here you can run the maximum amount of data without bagging. It takes a resonable amount of time to run. It took us less than 10 minutes with all 50000 data points.

### SVC
SVC takes a lot of computational power. Running the maximum set without grid search takes multiple hours. We choose to test a maximum of 10 000 when running no bagging and with grid search.

Avoid running grid search with large data amounts, this takes a lot of power and should require a dedicated server rather than a normal desktop computer.

A good amount of data points is around 1000-5000 for running multiple tests. However if the amount of data is that small, a great result can't be expected and a lot of variation can occur. An average over multiple runs would be best, but is very computational expensive.

## CNN different Optimizers 
We tried using 5 different optimizers for our CNN where we found that Adamax and Adam where the best performing once. The optimizers tested where Adam. Adamax, SGD, Adadelta and Ftrl with the following results using 50k data and 10 epochs 

| Optimizers | Accuracy |
|--|--|
| Adam  | 70.3% |
| Adamax | 70.69% |
| SGD | 57.49% |
| Adadelta | 13.26% |
| Ftrl | 10% |

There are other optimizers available you can find them at: **[https://www.tensorflow.org/api_docs/python/tf/keras/optimizers](https://www.tensorflow.org/api_docs/python/tf/keras/optimizers)**

## CNN different activation functions 
We also tried different activation functions on our CNN model where all tests ran with 50 000 data points, 10 epochs and the optimizer "Adam". The functions we tried where Relu, Gelu and Sigmoid. As a result Relu and Gelu preformed the best.

| Activation functions | Accuracy |
|--|--|
| Relu | 70% |
| Gelu | 71% |
| Sigmoid | 10% |

There are other functions available you can find at: **[https://www.tensorflow.org/api_docs/python/tf/keras/activations](https://www.tensorflow.org/api_docs/python/tf/keras/activations)**
 
## CNN Run with/without Dropout
We also ran our network with dropout to reduce the overfitting in the model. We ran with 0.4 dropout we did not get a increase in overall accuracy. We can see that the graph showing the run with droput has the accuracy closer to the val_acuraccy. 

## Graphs from the CNN runs
### Without Dropout
![enter image description here](https://raw.githubusercontent.com/anton-linden/D7041E-project/main/Resources/without-dropout.png)

### With Dropout
![enter image description here](https://raw.githubusercontent.com/anton-linden/D7041E-project/main/Resources/with-dropout.png)

## Results
![enter image description here](https://raw.githubusercontent.com/anton-linden/D7041E-project/main/Resources/Results.png)
