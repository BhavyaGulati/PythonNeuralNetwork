# PythonNeuralNetwork
3 Layer neural network built using python - Numpy
Description of the project :
1. We need to Import Numpy
2. Declare Signoid function, Its a function that maps any value to value between 0 and 1
   This is particularly usefull for creating probabilities out of numbers.
3. Initialise input data. Lets say our input is            ([[0,0,1]
                                                             [0,1,1]
                                                             [1,0,1]
                                                             [1,1,1]])
   It means we have 4 training examples with 3 neurons each.
4. As we are generating random numbers, We seed them to make them deterministic.
5. We define 2 layers of synopses for 3 layered neural network.
6. Formulating training code: We create a for loop that iterates over our training code to optimisa the n/w for given data        set.
   * First layer is our input data.
   * Prediction step involves performing matrix multiplication b/w each layer and its synopse. Then we run signoid function on      all the values of our matrix to form our next layer.
   * Next layer now contains prediction of our output data.
   * We reapply the same process to to this layer now to get even more precise prediction
7. Now that we have output value in layer2, we formulate error of layer2 as l2error=output-l2
8. Print average error at a set interval to assure that it goes down every time.
9. Multiply layer 2 error by our sigmoid function. This gives a derivative of output prediction from layer 2.
10. This delta2 is used to reduce the error rate of our predictions when we update our synopses every iteration.
11. Back Propogation: 
    Then if we want to know how much layer 1 contributed to error in layer2 we multiply layer2Delta by synopses1's Transpose.
12. Multiply layer 1 error by our sigmoid function. This gives a derivative of output prediction from layer 1.
13. Gradient Descent: We use both these deltas to update the synopses
14. l2 is the final output!!!
