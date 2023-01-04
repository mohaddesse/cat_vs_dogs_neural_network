# cat_vs_dogs_neural_network

the purpose of this programming is classification cats and dogs with and without neural network

- for neural network, I don't use libraries. I've implemented gradient descent in deep learning. it was so fun to understand how actual it works :)) 
- for classification I used to linear regression with and without sklearn library.

## collecting data

- link download: https://www.kaggle.com/competitions/dogs-vs-cats/data

there is a lot of data!! I can't use all of them with my little laptop!!!
and actually, the main purpose of this programming is to create a neural network step by step and verify hyperparameters ex: learning rate, number of iterations, number of layers, and number of neurons.
in collect_data.ipynb I sample data in 500,1000,3000 examples. instead of 25000 examples!!! for read images and save data I used **CV2** library

## classification without neural network

in classification_without_neural.ipynb there is 2 parts:

- first part: classify pictures with 500,1000,3000 examples:  
 in this part, I've implemented gradient descent for logistic regression with a sigmoid function. 
 
  - there are 5 functions for calculating weights, calculating costs, updating weights according to cost, and after finding the best weights, it predicts the target.
 I know the results it not so okay!! but I have a hardware solution!
 
  - there are some results for 3000 examples: it shows accuracy for test and train examples for different iterations and learning rates.

![Screenshot from 2023-01-04 14-46-39](https://user-images.githubusercontent.com/36596572/210545584-b9fb6e23-b167-4267-9bea-1e6dcc714224.png)

   - There are some results for 500 examples:  As you can see in the data frame accuracy for training examples is almost 100 % it is high variance and it needs regularization :))

![Screenshot from 2023-01-04 17-13-31](https://user-images.githubusercontent.com/36596572/210568087-8fa3dc67-6fb6-4754-9744-95cf66a7227c.png)

- second part: I've used **scikit learn** library logistic regression and **GridSearchCV**
![Screenshot from 2023-01-04 17-19-07](https://user-images.githubusercontent.com/36596572/210569301-d8daea28-172a-4182-b222-c9a2e98a69bc.png)
> the best result ==> alpha=0.001,num of iterations=6000, number of samples=1000 ==> accuracy test=64.0	accuracy train=87.000	

