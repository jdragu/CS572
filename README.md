# CS572
Plant Identification Final Project

## CNN Model 

This code is designed to predict plant traits using both tabular data and image data. It uses a combination of a custom Convolutional Neural Network (CNN) and tabular data processed through Dense layers to make these predictions. The model is trained to perform multi-target regression on six target variables.

### Main Functionalities

1. **Data Loading and Cleaning**: The code begins by loading the tabular data (train.csv and test.csv) and performs some basic cleaning operations, such as dropping certain columns and removing outliers.

2. **Image Data Processing**: The code uses the EfficientNet model pre-trained on ImageNet to process the image data. It creates a TensorFlow dataset from the image paths, processes the images, and extracts features using the EfficientNet model.

3. **Model Training**: The code trains a separate LightGBM model for each target variable in the tabular data. It uses early stopping to prevent overfitting.

4. **Prediction and Submission Preparation**: Finally, the code makes predictions on the test set using the trained models and prepares a submission file.

5. **Test Data Preparation**: The code normalizes the tabular test data in the same way as the training data was normalized. It then creates TensorFlow datasets for the image and tabular data, and zips these two datasets together.

6. **Prediction**: The code uses the trained model to make predictions on the test set. It batches the test dataset and feeds it into the model's `predict` method.

7. **Post-processing**: The code converts the predictions into a DataFrame and concatenates it with the test DataFrame. It also checks for any NaN values in the predictions.

8. **Denormalization**: The code then denormalizes the predictions to bring them back to the original scale. This is done by reversing the standardization that was applied during the training phase.

### Files

The main script is a single Python file that includes all the functionalities mentioned above. It imports several libraries such as os, sys, pandas, numpy, tensorflow, etc. The main data files it interacts with are:

- `train.csv`: The training data file.
- `test.csv`: The test data file.
- `train_images`: A directory containing the training images.
- `test_images`: A directory containing the test images.

### How to Run

To run this code, you need to have Python installed along with the libraries mentioned in the import statements. You also need to have the data files in the correct directories. Once everything is set up, you can run the script using a Python interpreter. I ran the code in Kaggle.

## XGBoost Tree Model

This code is designed to predict plant traits using both tabular data and image data. It uses a combination of LightGBM, a gradient boosting framework that uses tree-based learning algorithms, and EfficientNet.

### Main Functionalities

1. **Data Download and Extraction**: The code begins by downloading and extracting data from specified URLs. It handles both zip and tar files and saves the extracted files to a specified directory.

2. **Data Loading and Cleaning**: The code then loads the tabular data (train.csv and test.csv) and performs some basic cleaning operations, such as dropping certain columns and removing outliers.

3. **Image Data Processing**: The code uses the EfficientNet model pre-trained on ImageNet to process the image data. It creates a TensorFlow dataset from the image paths, processes the images, and extracts features using the EfficientNet model.

4. **Model Training**: The code trains a separate LightGBM model for each target variable in the tabular data. It uses early stopping to prevent overfitting.

5. **Prediction and Submission Preparation**: Finally, the code makes predictions on the test set using the trained models and prepares a submission file.

### Files

The main script is a single Python file that includes all the functionalities mentioned above. It imports several libraries such as os, sys, pandas, numpy, lightgbm, tensorflow, etc. The main data files it interacts with are:

- `train.csv`: The training data file.
- `test.csv`: The test data file.
- `train_images`: A directory containing the training images.
- `test_images`: A directory containing the test images.

### How to Run

To run this code, you need to have Python installed along with the libraries mentioned in the import statements. You also need to have the data files in the correct directories. Once everything is set up, you can run the script using a Python interpreter. I ran the code both in Kaggle and Google Colab using an L4 GPU.
