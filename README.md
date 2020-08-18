# Russian-Letters
This project is about classifying Russian letters. In total, there are 33 categories of Russian letters.
The goal of this project is to classify images among 33 different Russian letter categories.
The dataset can be found at this link: https://www.kaggle.com/olgabelitskaya/classification-of-handwritten-letters
It was prepared and uploaded by Olga Belitskaya, includes a total of 14190 images.

The Dataset contains three image folders: Letters, Letter2, Letter3, and its corresponding CSV files: letter1.csv, letter2.csv, letter3.csv.

Letters2 Image folders contains 5940 Russian letter images, with 180 images for each class with no background.
Letters3 Image folder contains 6600 Russian letter images,  with 200 images for each class with graph type background(i.e. filled with many horizontal and vertical lines).
Letters Image folders contains 1650 Russian letter images, with 50 images for each class and the backgrounds are mixed, some are gridded (few horizontal and vertical lines) and some are stripped(Only a few horizontal lines).
Russian alphabets are represented with numeric labels in the CSV files.

Letters >> Labels :
а=>1, б=>2, в=>3, г=>4, д=>5, е=>6, ё=>7, ж=>8, з=>9, и=>10,
й=>11, к=>12, л=>13, м=>14, н=>15, о=>16, п=>17, р=>18, с=>19, т=>20,
у=>21, ф=>22, х=>23, ц=>24, ч=>25, ш=>26, щ=>27, ъ=>28, ы=>29, ь=>30,
э=>31, ю=>32, я=>33

The Project Notebook is divided into 4 sections:
1.)Importing Monk library
2.)Importing Kaggle Dataset
3.)Data parser to ingest, explore, and visualize samples
4.)Developing different models

Firstly, I have prepared the handwritten image data then used Convolution Neural Networks and Transfer Learning techniques to build different models for letter classification. The models are then compared. 
The code is written in Google Colaboratory Notebook 
Monk library is used in this project
MXNet Gluon API is used as Backend 

Conclusion:
we have performed Transfer learning using various architectures, created an approach to build a solid classifier. Although there is one thing to be noted here that creating projects and experiments made it very easy to manage and compare experiments. Resnets also performs second best to Densenets while Mobilenets can potentially perform very well if worked on, although it took a lot of training time and space for this task.

Finally, We got a hard to beat validation performance from our DenseNet_121 model.

If there are any improvements that we could do in the present model, it will be focusing on improving/increasing the images with graphic type backgrounds. This is because after those images are added and the model is trained, the model doesn't perform as good as earlier.
These are some areas of work that can be explored to further increase the performance of the model.


#Initial Requirements 

1.)Clone MonkAI repository:

 ! git clone https://github.com/Tessellate-Imaging/monk_v1.git

2.)Installing Requirements :
For Colab Notebook,

! cd monk_v1/installation/Misc && pip install -r requirements_colab.txt
