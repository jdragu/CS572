# CS572
Plant Identification Final Project

## CNN Model 



## XGBoost Tree Model

This code is designed to predict plant traits using both tabular data and image data. It uses a combination of LightGBM, a gradient boosting framework that uses tree-based learning algorithms, and EfficientNet.

## Main Functionalities

1. **Data Download and Extraction**: The code begins by downloading and extracting data from specified URLs. It handles both zip and tar files and saves the extracted files to a specified directory.

2. **Data Loading and Cleaning**: The code then loads the tabular data (train.csv and test.csv) and performs some basic cleaning operations, such as dropping certain columns and removing outliers.

3. **Image Data Processing**: The code uses the EfficientNet model pre-trained on ImageNet to process the image data. It creates a TensorFlow dataset from the image paths, processes the images, and extracts features using the EfficientNet model.

4. **Model Training**: The code trains a separate LightGBM model for each target variable in the tabular data. It uses early stopping to prevent overfitting.

5. **Prediction and Submission Preparation**: Finally, the code makes predictions on the test set using the trained models and prepares a submission file.

## Files

The main script is a single Python file that includes all the functionalities mentioned above. It imports several libraries such as os, sys, pandas, numpy, lightgbm, tensorflow, etc. The main data files it interacts with are:

- `train.csv`: The training data file.
- `test.csv`: The test data file.
- `train_images`: A directory containing the training images.
- `test_images`: A directory containing the test images.

## How to Run

To run this code, you need to have Python installed along with the libraries mentioned in the import statements. You also need to have the data files in the correct directories. Once everything is set up, you can run the script using a Python interpreter. I ran the code both in Kaggle and Google Colab.
