# Automated-segmentation-and-classification-of-plant-leaves
This project is to design a program for the automated segmentation and classification of plant leaves. The program’s input is a plant leaf image, and the output should consist of 1) A binary image with only the plant leaf object, and 2) The class of the plant leaf image. The dataset consists of 10 plant classes.

It was required to segment all images in the given dataset. You will find the dataset in a zip file named “_Output.zip”.
- The images in the given dataset are low contrasted images and have some salt and pepper noise. 
So, to segment the images you need to do some preprocessing, you may need to: 
    • Adjust the contrast of the image. o Remove the salt and pepper noise. o Extract the plant leaf region using Thresholding or any other segmentation technique.
    • Use morphological operations (Erosion, Dilation, Opening, Closing, …) to further improve the segmentation result.
    • To assess your segmentation result, you will need to measure the average Intersection of Union (IoU or Jaccard index) between your segmentation output and the              ground truth segmentations provided in the zip file named “_Ground_Truth.zip”. The Jaccard index is a value between [0-1] (the higher the better matching). We do this for all images in the dataset and calculate the average Jaccard index, which indicates the overall segmentation accuracy of your program.

2. Take the output segmented binary images and extract some meaningful features for each image such as:
     • Boundary Features (e.g., Fourier Descriptors).
     • Region Features (e.g., Area, Perimeter, Circularity, Convexity, Compactness, Moments, …etc.).
     • The extracted features for all images in the dataset should be inserted into a features table where the records correspond to the images and the columns correspond
     to the extracted features. This features table is then divided into training and test sets. 
     • Finally, we train some classifier on the training set and evaluate its accuracy on the test set. 
The output should be 1) a trained classifier model with its accuracy figure on the test set, and 2) the predicted class for a given input image using the trained classifier.
