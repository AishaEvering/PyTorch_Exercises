<p align="center">
   <img src="https://github.com/AishaEvering/PyTorch_Exercises/blob/main/header_2.png" alt="PyTorch Logo" width="600" height="300">
</p>

# Transfer Learning
<sup>[Go to Read Me](https://github.com/AishaEvering/PyTorch_Exercises/blob/main/README.md)</sup>

Breaking code into python scripts for reusability.

## Technologies
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
[![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)](https://matplotlib.org/)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

## 📙 [Jupyter Notebook](https://github.com/AishaEvering/PyTorch_Exercises/blob/main/06_pytorch_transfer_learning_exercises.ipynb)

* **🔑 Key Takeaways**
   * I'm not new to transfer learning but doing it with PyTorch seems to be much more straight forward.
   * When choosing a a base model consider the...
      * Speed - How fast does it run?
      * Size - How big is the model?
      * Performance - How well does it handle your chosen problem.
         * Where does the model live?  On a server with a lot of compute or on a mobel app?
    * After that it's all about transforming the data correctrly.
    * Then updating your classifier layer (in my case) to have the correct number of output features.
    * Easy Peasy

* **😤 Where I Got Stuck**

  * There are multiple ways of training a model.  When I tried the way of using weights.transform to train my data things did not go well. (Update
) I figured it out.  It's the best way to go just in case the recipe for transforming the data for the base model changes.
 
* **🤓 TIL (I have my hand in several aspects of Machine Learning so sometimes I will come across something I thought was cool and need a place to remember it.  This is that place.)**

  * I've come to the conclusion that most models are using transfering learning from bigger models these days.  Why start from scratch?  No reason.
