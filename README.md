<p align="center">
   <img src="https://github.com/AishaEvering/FaceVerification/blob/main/FaceVerification.png" alt="Face Verfication" width="600" height="300">
</p>

# Face Verification (YouTube Tutorial) :youtube

This is the result of an 8 part YouTube series of using Deep Learning with TensorFlow to authenicate your face much like on IPhone.  *Pretty Cool.*

## Technologies
[![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)](https://matplotlib.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/stable/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)](https://www.tensorflow.org/)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

## 📃Description

This is a TensorFlow neural network model that performs computer vision to authenticate an image.

## 🏫 What Did I Learn

* How to use Tensor flow decoraters.
* How to create a custom training step using TensorFlow.

## 🔑 Key Takeaways

This is my first experience with following a research paper's neural network archetecture.  Some of the cool takeways I got from it where
* One Shot: The model must correctly make predictionss given only a single example.  The model was trained on hundreds of images of my face (positive) and randomn faces (negative). Then the model was given a single single (one-shot) image and validated it against a validation image.  Depending on the verfiication threshold which in the case was 70% the model verified that if the person in the image was the same person if the given image.
* This model used the siamese neural network method that took in 2 inputs and ranked the similarity.


### 😤 Where I Got Stuck

* OpenCV opening the web camera does not work in Google Colab.  There is a snippet available on Google Colab that takes a single picture from the web camera, but I needed hundreds.  So I took a little detour and updated the code to work like OpenCV did in the tutorial.  I even wrote about it, check it out. [TIL How to Take Hundreds of Images Through Google Colab](https://dev.to/aishaevering/til-how-to-take-hundred-of-images-through-google-colab-3bbo)

### ☑️ Todos...

* Deploy the model so it can easily verfiy faces.
  
### 📖 Dataset

* ~400 Anchor images taken with my webcam.  They are currently stored in my Google Drive.
* ~400 Positive images taken with my webcam.  They are currently store in my Google Drive.
* ~400 Negatvie images provided my tutorial, labled Faces in the Wild. 
  
## 🙏 Acknowledgments

* [Nicholas Renotte]([https://github.com/matiassingers/awesome-readme](https://www.youtube.com/watch?v=bK_k7eebGgc&list=PLgNJO2hghbmhHuhURAGbe6KWpiYZt0AMH))
* 📑 [Siamese Neural Network for One-shot Image Recognition]([https://gist.github.com/PurpleBooth/109311bb0361f32d87a2](https://www.cs.cmu.edu/~rsalakhu/papers/oneshot1.pdf))
