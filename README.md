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


- There are some results for 1000 examples:

![Screenshot from 2023-01-04 18-00-34](https://user-images.githubusercontent.com/36596572/210581954-c5debbb1-6e35-47ae-8bfb-b48a99e91c5d.png)



- second part: I've used **scikit learn** library logistic regression and **GridSearchCV**

![Screenshot from 2023-01-04 18-29-39](https://user-images.githubusercontent.com/36596572/210584704-eab18f05-1e4a-4d19-9fc2-385ba9f3f8bd.png)


> the best result with own created algorithms ==> alpha=0.001,num of iterations=6000, number of samples=1000 ==> accuracy test=64.0	accuracy train=87.000	

## classification with neural network

 in classification_with_neural_network.ipynb I've implemented gradient descent in deep learning.
- in this part I've written a couple of functions:
  - to initialize weights w,b for L layer neural network
  - to calculate forward equations for L layers
  - to calculate backward propagation for gradients descent
  - update parameters according to cost functions and derivative
  - and finally predict functions
  
 - **we can see some results together:**


  > learning rate=0.0015 and num of iterations: 2500 ==> alpha is too small and cost decrease slowly.
 
![Screenshot from 2023-01-04 18-09-37](https://user-images.githubusercontent.com/36596572/210582113-7fee47ca-7438-49fc-8a4a-0b861dc77f9a.png)

  
  > learning rate=0.01 and num of iterations: 2500 ==> result is getting better with increase learning rate


![Screenshot from 2023-01-04 18-16-53](https://user-images.githubusercontent.com/36596572/210582201-24a79def-1598-4e09-8425-514adb1a903a.png)

  > learning rate=0.02 and num of iterations: 2200 ==> ok result is pretty good with increase learning rate

![Screenshot from 2023-01-04 18-23-55](https://user-images.githubusercontent.com/36596572/210582380-aed152a7-b759-4701-ab11-8dcbebde0a91.png)


  > learning rate=0.03 and num of iterations: 2500 ==> oh no cost function oscillate because learning rate is large!!
  
  ![Screenshot from 2023-01-04 18-24-03](https://user-images.githubusercontent.com/36596572/210582413-f630f488-cb21-4b27-b4ec-1411630b91fa.png)

