<p align="center">
   <img src="https://github.com/AishaEvering/PyTorch_Exercises/blob/main/header_2.png" alt="Face Verfication" width="600" height="300">
</p>

# PyTorch Excersises

This repo will contain all exercises I did that cover different aspects of working with PyTorch.  If you are reading this thanks for watching me grow. 😄

## Technologies
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
[![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)](https://matplotlib.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/stable/)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

## 📃 Description

This repo contains different aspects of PyTorch, what I learned, what finally clicked, and what took a minute.
  
## 📚 [Fundamentals (Tensors)](https://github.com/AishaEvering/PyTorch_Exercises/blob/main/00_pytorch_fundamentals_exercises.ipynb)
   * **📄 Description**

     I did these exercises to solidify the basics of working with Tensors.
     
   * **🔑 Key Takeaways**
     * Device agnostic code is very very important.  It's best to set the device early in the project to make it easier to handle any device specific errors later.
     * Matplotlib does not support cuda.  You have to go back to `...cpu()` in order to plot something.
     *  This is how you multiply a tensor, `tensor_1.matmul(tensor_1.T)`.  So is this, `tensor_1.mm(tensor_1.T)`. And this, `tensor_1 @ tensor_1.T`

   * **😤 Where I Got Stuck**
      * Why do we have to randomly squeeze tensors?  I understand the squeezing a tensor removes the 1 deminsions.

## 📚 [Linear Regression](https://github.com/AishaEvering/PyTorch_Exercises/blob/main/01_pytorch_workflow_exercises.ipynb)
   * **📄 Description**

     With these exercises I created linear data using `torch.arange`, built a linear regression model, created a testing and training loop, made predictions, plotted the predictions, saved the model to disk, and loaded the model.

   * **🔑 Key Takeaways**
       * `nn.L1Loss()` is MAE (Mean Absolute Error).  This is the loss function for regression models. Basically, how far on average where the predictions off from the ground truth?
       * SGD Optimizer (Stochastic Gradient Descent) works with a lot of model types including linear regression.  It changes the model's parameters (weights, bias) **using a subset of the training data** in order to lower the loss/cost function.
       * Set to Train Mode, Forward Pass, Calculate the Loss, Zero the gradients, Back Propagation, Optimizer Step
       * When testing or making predictions be sure to put the model in eval mode so it doesn't so extra uneeded steps like gradient descent, dropout, etc..
       * Also when testing or making predictions use `with torch.inference_mode():` for faster processing
       * It's recommended to save the stat_dict instead of the entire model.
       * When saving the best model be sure to use `deepcopy(model.stat_dict())` or the best_model will be updated as the model continues to train.

   * **😤 Where I Got Stuck**
       * Squeezing and Unsqueezing tensors still seem a little unintuitive.  I recongnize the error so the fix is quick but I will like when to squeeze/unsqueeze to become more intuitive.
    
         
## 📚 Binary & Multiclass Classification
   * **📄 Description**

        These excersises consist of creating binary and multiclass classification models. Also I have to choose the appropriate loss and optimization functions.

   * **🔑 Key Takeaways**
        * I've used Relu before but somehow these exercise really brought home what non-linearity really means.  If you have a regression line or some classification data that can be seperated with a straight line then you don't need ReLu or any other non-linear activation function.  I understood that it took the max(0, x) before essentially turning off neurons.  But to plot it and see the lines curve was a click momment for me.
        * LeakyRelu is supposed to be better because it doesn't turn the neurons completely off.
        * Using the Sequential container to chain the layers within the nnModule makes writing the forward function a lot easier.
        * I understand that you can build a model with the sequential container alone.  Creating s nn.Module subclass is good practice for now.
        * Activation functions are not hard to right but PyTorch somehow makes them more effecient.
        * Binary Classification
           * BCEWithLogitsLoss loss function is "numerically stable" than just using the BCELoss function.  Accordinig the the PyTorch documentation.
           * BDEWithLogitsLoss call Sigmoid followed by BCELoss.  Otherwise in order to call BCELoss you have to call Sigmoid first.
           * For Binary classification to first have to forward pass causing the model to return the raw logits.  Then call the sigmoid function which changes them to values between 0 and 1.  Then round those values and BOOM you have predictions that look like you y labels.
           * I read that the better activation function is `tanh()`  because it's zero center but can be computationallu expersive.
        * Multiclass Classification
           *    Accuracy is a easy calculations but I used the TorchMetrics Accuracy instead.  Of course I usually use the one from Scikit-Learn.
           *    Instead of SGD I used the Adam optimizer instead and increased the learning rate.  This returned a really great test accuracy.
           *    For Multiclass classification to first have to forward pass causing the model to return the raw logits.  Then call the softmax function which changes them to probabilities that add up to 1.  After that call `argmax()` to get the highest probability.
   * **😤 Where I Got Stuck**

      * Sometimes I'll walk away and when I run the same code I get an error that the tensor is not on the correct device.  I could just at `...to(device)` at the end but there's no real need the code was working perfectly fine before.  If I rebuld the model everything is back to normal.
      * Make sure you get the in_features, and out_features correct.  I mis-read my binary y label as 2 instead of the layer should return 1 value.  Found the issue and fixed it.

## 🙏 Acknowledgments

* [Daniel Bourke](https://github.com/mrdbourke)
