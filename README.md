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


## Requirements & Versions
Python: 3.10
Tensorflow: 2.9.2
Matplotlib: 3.6.2
Opencv-python: 4.6.0.66

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
