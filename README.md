# Russian-Letters
This project is about classifying russian letters using different classical networks. In total , there are 33 categories of russian letters which is present in the dataset.
The goal of this project is to classify images among 33 different russian letter categories.

The code is written in Google Colaboratory Notebook and the dataset can be found at this link : https://www.kaggle.com/olgabelitskaya/classification-of-handwritten-letters.
The dataset was prepared and uploaded by Olga Belitskaya including total of 14190 images

The Dataset contains three image folders namely : Letter1 , Letter2 , Letter3 and its corresponding csv files.
Letter1 Image folders contains 1650 russian letter images, with 50 images for each class and the background for the images are same which is indicated by 2 horizontal lines.  
Letter2 Image folders contains 5940 russian letter images , with 180 images for each class and the background for the images is plain white.
Letter3 Image folder contains 6600 russian letter images ,  with 200 images for each class and the background for each image is grid type (i.e. with multiple vertical and horizontal lines)

Russian alphabets are represented with numeric labels in the csv files.
Letters >> Labels :
а=>1, б=>2, в=>3, г=>4, д=>5, е=>6, ё=>7, ж=>8, з=>9, и=>10,
й=>11, к=>12, л=>13, м=>14, н=>15, о=>16, п=>17, р=>18, с=>19, т=>20,
у=>21, ф=>22, х=>23, ц=>24, ч=>25, ш=>26, щ=>27, ъ=>28, ы=>29, ь=>30,
э=>31, ю=>32, я=>33

The Project Notebook is divided into 4 different sections:


Firstly, i have prepared the handwritten image data then i have used Convolution Neural Networks and Transfer Learning techniques to build different models for letter classification.
Then there is comparison between different model and then the best model is further developed.
The Library used for this project is Monkai library.

#Getting Started 

1.)Clone MonkAI repository:

 ! git clone https://github.com/Tessellate-Imaging/monk_v1.git

2.)Installing Requirements :
For Colab Notebook,

! cd monk_v1/installation/Misc && pip install -r requirements_colab.txt


Accuracy using different deep learning Classical Networks :












