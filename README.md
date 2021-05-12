# Assignment 1 - Medical Pattern Recognition - HEMN451
## Made by :

| Name | ID |
| ------ | ----------- |
| Hoda Hossam Monier   | 1170156 |
| Mohammed Nader Ahmed | 1170366 |

# **Description of both algorithms :**
```
Batch perception algorithm works as following:
1. Learning rate is intialized to 1
2. Intialie weights with random values between [-1,1]
3. Intialize an error value [delta] to change the weights until it reaches the best condition.

Weights will be continusoly changing "creating more epochs" until the delta value reaches a very small number [epsolin = 2.220446049250313e-16], and delta value will change depending on the value of [Y.W.X] if it's less than or equal zero by the following equation:
Delta [new] = Delta[old] - [Y.X]

Each time weight changes by the follwoing equation:
W [new] = W[old]-(LR*Delta)

The process of changing weights values happens only once at each epoch after normalizing the delta value using the previously stated equation. 
 
The output of this algorithm will be the final weights for each feature in the features vector with accuracy +75%.  
```
<img src="/Images/Batch_Pcode.jPG", width=800>
![Batch Perceptron Algorithm](/Images/Batch_Pcode.jPG)

---

```
Online Training Algorithm works with the same concept as the Batch persceptron algoritm, except that:

The process of changing weights values happens many times at each epoch which will reudces both running time and number of epochs, and it also increases the efficiency of the training model.

The output of this algorithm will be the final weights for each feature in the features vector with accuracy +80%. 
 
```


![Online Training Algorithm](Images/Onlinebatch_Pcode.JPG)

# **Implemented Methods :** 

This function returns a float with the magnitude (absolute value) of A but the sign of B.
```py
sign = lambda x: math.copysign(A,B)
```

# **Results**

## **Part - 1 (Sheet problems)**

### Batch Perceptron Algorithm - Problem 1 :
```
Weights :  [ -5.27  484.515]
Number of each time algorithm updated model weights :  2421
Number of epochs :  2421
```
![Batch Perceptron Algorithm Prob 1](Images/Batch_Perceptron_Prob1.jPG)

---

### Online Training Algorithm - Problem 1 :

```
Weights :  [-0.13070313 10.67917969]
Number of each time algorithm updated model weights : 203
Number of epochs : 67
```
![Online Training Algorithm Prob 1](Images/Online_Algorithm_Prob1.jPG)


### **Comments**
```
Online algorithm was extremely faster and more accurate as it had only 67 epochs compared to 2421 in Batch Preceptron algorithm.
```
---

### Batch Perceptron Algorithm - Problem 4 :

```
Weights :   [-64.02   32.355  63.52    0.145]
Number of each time algorithm updated model weights : 6
Number of epochs : 6
```
![Batch Perceptron Algorithm Prob 4](Images/Batch_Perceptron_Prob4.jPG)

---

### Online Training Algorithm - Problem 4 :

```
Weights :   [-4.04017969e+01  2.75025781e+01  3.18053027e+01  1.80969238e-02]
Number of each time algorithm updated model weights : 8
Number of epochs : 4
```

![Online Training Algorithm Prob 4](Images/Online_Algorithm_Prob4.jPG)

### **Comments**
```
Here both algorithms were very close to each other at many cases as one has 6 epochs and the other has 4.
```
---

## **Part - 2 (Make_classifcation function)**

### Batch Perceptron Algorithm :  
- Train set

```
Weights :   [-0.31459554  0.68142681]
Number of each time algorithm updated model weights : 3
Number of epochs : 3
```
![Batch Perceptron Algorithm Train](Images/Batch_MakeClass_Train.jPG)

---

- Test set

```
Accuracy of the model is :  1.0
```

![Batch Perceptron Algorithm Test](Images/Batch_MakeClass_Test.jPG)

---

### Online Training Algorithm : 
- Train set

```
Weights :   [0.24610127 0.88789378]
Number of each time algorithm updated model weights : 8
Number of epochs : 3
```
![Online Training Algorithm Train](Images/Online_MakeClass_Train.jPG)

---

- Test set

```
Accuracy of the model is :  1.0
```

![Online Training Algorithm Test](Images/Online_MakeClass_Test.jPG)

---
**NOTE**

Result will differ every time you run the code, as the weights given in the function are random between [-1,1]

---
