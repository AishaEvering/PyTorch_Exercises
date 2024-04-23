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
       * When saving the best model be sure to use `deepcopy(model.stat_dict()) or the best_model will be updated as the model continues to train.

   * **😤 Where I Got Stuck**
       * Squeezing and Unsqueezing tensors still seem a little unintuitive.  I recongnize the error so the fix is quick but I will like when to squeeze/unsqueeze to become more intuitive.
    
         
## 📚 Binary & Multiclass Classification
   * **📄 Description**

   * **🔑 Key Takeaways**

   * **😤 Where I Got Stuck**

## 🙏 Acknowledgments

* [Daniel Bourke](https://github.com/mrdbourke)
