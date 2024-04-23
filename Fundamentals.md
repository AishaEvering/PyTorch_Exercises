<p align="center">
   <img src="https://github.com/AishaEvering/PyTorch_Exercises/blob/main/header_2.png" alt="Face Verfication" width="600" height="300">
</p>

# Fundamentals (Tensors) 
<sup>[Go to Read Me](https://github.com/AishaEvering/PyTorch_Exercises/blob/main/README.md)</sup>

Solidifying the fundamentals of Tensors and Pytorch 😄

## Technologies
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
[![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)](https://matplotlib.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/stable/)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

## 📙 [Jupyter Notebook](https://github.com/AishaEvering/PyTorch_Exercises/blob/main/00_pytorch_fundamentals_exercises.ipynb)

   ❓What is a Tensor?:<br>
    Tensors are n-dememsional arrays with the implicit assumption that they ca run on a GPU.  They are fast.  Way faster than arrays.

   * **🔑 Key Takeaways**
     * Device agnostic code is very very important.  It's best to set the device early in the project to make it easier to handle any device specific errors later.
     * Matplotlib does not support cuda.  You have to go back to `...cpu()` in order to plot something.
     *  This is how you multiply a tensor, `tensor_1.matmul(tensor_1.T)`.  So is this, `tensor_1.mm(tensor_1.T)`. And this, `tensor_1 @ tensor_1.T`

   * **😤 Where I Got Stuck**
      * Why do we have to randomly squeeze tensors?  I understand the squeezing a tensor removes the 1 dimensions.
