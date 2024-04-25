<p align="center">
   <img src="https://github.com/AishaEvering/PyTorch_Exercises/blob/main/header_2.png" alt="PyTorch Logo" width="600" height="300">
</p>

# Computer Vision
<sup>[Go to Read Me](https://github.com/AishaEvering/PyTorch_Exercises/blob/main/README.md)</sup>

Here I am using PyTorch to build a computer vision model. I seem to gravitate towards computer vision projects.  Maybe because I like pictures.  I will add some vireity to my portfolio later but for now it's computer vision time. 👓

## Technologies
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
[![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)](https://matplotlib.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/stable/)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

## 📙 Jupyter Notebook TBD

* **🔑 Key Takeaways**
   * Besides creating your own there are a lot of ways to get data.  In this lesson I learned how to get data from PyTorch.  But there's also Kaggle, IBM, MNIST, so on and so on....
   * Finally started using the dataloader which turns out not to be a big deal.  It just turns you dataset into a iterable.  I don't why I though it was something more.
   * Also Python function `iter()`
   * It's more efficient and less computationally expensive to work in batches.  Why put 60,000 tensors in memory and optimize (gradient descent) when you can put ~2000.
   * Also starting to focus on how long the model takes to train.  Because not only do models have to be somewhat accurate they also have to be fast.
   * *to be continued...*
* **😤 Where I Got Stuck**

  * I think I need to look out my print outs when the model it training.  I think I got a calculation wrong somewhere.
  * *to be continued...*
 
* **🤓 TIL**

  * I cam across this today and I don't want to forget it.  It has nothing to do with Computer Vision though, it's more about EDA.  
    Have you heard of `DataFrame.melt()` I've been studying a lot and I've until today, no one mentioned it.  It's really cool.  It takes a list of columns and "melts" them into rows.  Which makes visualizing the data really cool.

   Snippet I don't want to forget:<br>
   ```
  features = ["YearBuilt", "MoSold", "ScreenPorch"]

   sns.relplot(
       x="value",
       y="SalePrice",
       col="variable",
       data=df.melt(id_vars="SalePrice", value_vars=features),
       facet_kws=dict(sharex=False),
   );
   ```
