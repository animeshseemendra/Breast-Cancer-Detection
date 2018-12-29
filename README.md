# Breast-Cancer-Detection
Udacity Capstone Project and Proposal 
# Background
Breast Cancer is the most common type of cancer in woman worldwide accounting for 20% of all cases. In 2012 it resulted in 1.68 million new cases and 522,000 deaths. One of the major problems is that women often neglect the symptoms, which could cause more adverse effects on them thus lowering down the survival chances. In developed countries the survival rate is although high, but it is an area of concern in the developing countries where the 5-year survival rates are poor. In India, there are about one million cases every year and the five-year survival of stage IV breast cancer is about 10%. Therefore it is very important to detect the signs as early as possible. 

# Problem
The idea is to use pathology test images and classify them as IDC(+) and IDC(-). Accurately identifying and categorizing breast cancer subtypes is an important clinical task, and automated methods can be used to save time and reduce error. The pathological tests include images of the tissues, the task is to train a computer to use these images and respond on whether the person is IDC(+) or IDC(-). Since it is a medical field problem it is important that sensitivity of the output should be high. 

# Solution 
Our data involves images with the classes written on data file name, therefore, we would need to extract the class name from it and create a column to store them. We also need to split the dataset into the  training set, validation set and testing set. Testing set for checking how good the model works on completely unseen data and validation set to check and avoid underfit or overfit, the will also help to select the best model. One hot encoding will be done in classes column so that it could work better with our model. Image processing step is also required to reduce the pixel range from 0-250 to 0-1. After it CNN model is to be used to predict the class, CNN creates an effective architecture   the 2D structure of the image, therefore, it would be the best to use, considering that we are working with the images.

# Data
The problem statement involves using images that are obtained during pathology tests to detect whether the patient is IDC positive or negative. Histopathology images are the images of tissues that are obtained during pathology tests, therefore, these images will act as inputs for the problem.
  The dataset that contains histopathology images for breast cancer is present on kaggle at : https://www.kaggle.com/paultimothymooney/breast-histopathology-images . The dataset contains 198,738 of negative IDC and 78,786 of positive IDC, therefore, it is a good dataset with enough data for our task. The original dataset consisted of 162 whole mount slide images of Breast Cancer (BCa) specimens scanned at 40x. However, the data that I have selected contains images that are cropped from the original dataset i.e it contains patches of regions where the IDC occurs, making it more specific to our problem. Each patch’s file name is of the format: u_xX_yY_classC.png — > example 10253_idx5_x1351_y1101_class0.png . Where u is the patient ID (10253_idx5), X is the x-coordinate of where this patch was cropped from, Y is the y-coordinate of where this patch was cropped from, and C indicates the class where 0 is non-IDC and 1 is IDC.

## Steps to follow:
1. Data is present in Kaggle link- https://www.kaggle.com/paultimothymooney/breast-histopathology-images
2. Create a notebook with this dataset.
3. Download the notebook *breast_cancer* and upload it on that notebook.
4. Run the notebook
 
 ## Required Libraries
 1. Numpy (NumPy is the fundamental package for scientific computing with Python Link : http://www.numpy.org/)
 2. Pandas (In computer programming, pandas is a software library written for the Python programming language for data manipulation and analysis. Link :https://pandas.pydata.org/)
 3. Glob ( The glob module finds all the pathnames matching a specified pattern according to the rules used by the Unix shell, although results are returned in arbitrary order. Link : https://docs.python.org/2/library/glob.html)
 4. PIL ( Python Imaging Library is a free library for the Python programming language that adds support for opening, manipulating, and saving many different image file formats. Link : https://pillow.readthedocs.io/en/5.3.x/ )
 5. Tqdm ( Instantly make your loops show a smart progress meter.  Link : https://pypi.org/project/tqdm/)
 6. cv2 ( OpenCV link : https://opencv-python-tutroals.readthedocs.io/en/latest/index.html)
 7. Matplotlib (matplotlib is a plotting library for the Python programming language and its numerical mathematics extension NumPy Link :https://matplotlib.org/)
 8. csv ( To read and write CSV files)
 9. IPython ( To display dataframe in a well formated form)
 10. sklearn ( It is used to provide metrics and test train split algorithms)
 11. Keras (Keras is used to built models)
 12. imblearn (It is used for providing undersampling link: https://pypi.org/project/imblearn/)
 13. itertools (This module implements a number of iterator building blocks inspired by constructs from APL, Haskell, and SML. Each has been recast in a form suitable for Python Link: https://docs.python.org/2/library/itertools.html)
