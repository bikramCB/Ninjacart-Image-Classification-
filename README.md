## Problem Statement

Ninjacart is India's largest fresh produce vegetables supply chain company, connecting producers(Farmers) directly with retailers. You are a Data Scientist at Ninjacart, you have curated a dataset consisting of some vegetables and other images at a vegetable market. You want to classify these images using computer vision with the most efficient and accurate model to integrate into your app. We will explore how to preprocess, load, and augment our raw data train state-of-the-art model architectures on it, and compare them to analyze the best model for our use case.
Ninjacart has provided us with datasets scrapped from the websites with train and test folders each having 4 sub-folders with images of onions, potatoes, tomatoes, and some market scenes. We have been tasked with preparing a multiclass classifier for identifying these vegetables

## Download datasets:
1. Download the Data (you can use gdown) from Google Drive with the provided Dataset Link and unzip it.
2. Visualize the data, and use the dataset directory to create a list containing all the image paths in the training folder. You can use Matplotlib or TensorFlow to plot a grid sample of the images you fetched from the list of image paths.
3. Plot a few of the images of each class to check their dimensions. image dimension is uneven.
4. Verify the count of images of each class in each train and test folder by plotting a histogram.
   Count of training samples per class:
            class  count        
0         tomato    789
1         potato    898
2  Indian market    599
3          onion    849
           Total    3135

   Count of testing samples per class:
            class  count
0         tomato    106
1         potato     81
2  Indian market     81
3          onion     83
           Total    351

6. Spliiting training datasets 80-20% from training and validation.
7. Make every image to (256,256) dimensions and also perform rescaling which will rescale the pixels of input images between 0-1 by dividing each value by 255.
8. Build a Custom CNN model with 5 Convolution layer with same size kernals (3x3). Apply GAP, Performed with Adam optimizer. And obtained precision, accuracy and recall for 20 epochs.
9. perform the model on test datasets , Plot confusion matrix and every class accuracy and aoverall accuracy 76% and loss 50% which is indicating model is over fitted.
10. To fix the overfitting apply data augmentation, batch normalization and dropout. Perform tune modeling on train data and val data for 14 epochs including best weights checkpoints and early stopping.
11. obtain accuracy 84% and loss 41%. And draw confusion matrix.
12. Apply transfer learning of VGG19, Resnet, Mobilenet to obtain different accuracy for different models.
13. Resnet giving the highest accuracy of 94% test accuracy and 99% train accuracy.
14.  
