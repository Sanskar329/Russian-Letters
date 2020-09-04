# Russian-Letters
The goal of this project is to classify images among 33 different Russian letter categories.

For indepth explanation of the project visit my blog for this project : 

https://medium.com/@sanskar329/russian-alphabets-classification-using-monk-ai-4df7d1ad8542#270f-83ebe5f745bc

Published by Towards Data Science Publications.

**About Dataset**

In total, there are 33 categories of Russian letters.
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

**The Project Notebook is divided into 4 sections:**

**1.)Importing Monk library**

**2.)Importing Kaggle Dataset**

**3.)Data parser to ingest, explore, and visualize samples**

**4.)Developing different models**

Firstly, I have prepared the handwritten image data then used Convolution Neural Networks and Transfer Learning techniques to build different models for letter classification. The models are then compared. 
The code is written in Google Colaboratory Notebook 
Monk library is used in this project
MXNet Gluon API is used as Backend 

**Approach**

Approach for training the model:

We have not concatenated the three image folders together and also the corresponding CSV files which could allow us to train the entire dataset together. This is because all three have slightly different types of backgrounds.

My approach to building a robust model is training the model first by using images that are least affected by the background i.e. second image folder.
Also, this folder is reasonably big (with a large number of images), so it can train the model effectively at first and we can understand how the model is performing with simpler data.

This would somewhat ensure if the model trains well and learns to extract desired features and we can verify this by analyzing plots for the same.
If it is observed that the model learns well when the background is white and has learned to extract features properly, then we can continue training the model with the next folder which contains images with graphic type background, this folder is also very big so hopefully, it makes the model learn to ignore the background. We can always analyze if the model does well in classifying this type or not.

Finally, we update and train the model with first folder images, containing gridded/stripped background.

This approach allows us to figure out which part of the dataset is not being classified properly and if we have unsatisfactory results, we can anytime analyze our plots and identify where the model is performing poorly and focus on that part.

Our Base approach for developing models :

1.)First, the backend was chosen (MXNet Gluon), then some basic models are selected from the available ones, which can be appropriate for this particular task.

2.)Then less dense networks are chosen among them and their performance is analyzed.

3.)After which the parameters are tuned for the models.

4.)We then obtained optimal parameters for these models and with the same parameters , more dense variants for the same model were   tried . This gives an idea as to which one performs better.

If we would have gone for very dense networks at first ,due to exploding/diminishing gradients it wouldn't perform well and we may end up not considering that option at all.

**Conclusion**
![Capture12345](https://user-images.githubusercontent.com/55439912/92220466-e9786f80-ee50-11ea-973c-3326d3f6f2c3.JPG)

we have performed Transfer learning using various architectures, created an approach to build a solid classifier. Although there is one thing to be noted here that creating projects and experiments made it very easy to manage and compare experiments. Resnets also performs second best to Densenets while Mobilenets can potentially perform very well if worked on, although it took a lot of training time and space for this task.

Finally, We got a hard to beat validation performance from our DenseNet_121 model.

If there are any improvements that we could do in the present model, it would be focusing on improving/increasing the images with graphic type backgrounds. This is because after those images are added and the model is trained, the model doesn't perform as good as earlier.
These are some areas of work that can be explored to further increase the performance of the model.


**Initial Requirements**

1.)Clone MonkAI repository:

 ! git clone https://github.com/Tessellate-Imaging/monk_v1.git

2.)Installing Requirements :
For Colab Notebook,

! cd monk_v1/installation/Misc && pip install -r requirements_colab.txt














