# Unsupervised Learning Challenge: Predicting Actions and Persons from Sensor Data

This project aims to predict actions and persons based on sensor data using unsupervised learning techniques. The provided dataset contains time-stamped sensor data along with corresponding actions and persons.

## Data Preprocessing

The provided dataset is preprocessed to reshape the data into a suitable format for analysis. Each sensor value is split into 50 segments, and additional columns are added to represent the sensor, action, and person for each segment. Various statistical features such as pulse indicator, energy, RMS, skewness, kurtosis, mean, standard deviation, median, and peak-to-peak (P2P) are computed for each segment. Fourier transformation and autocorrelation features are also extracted.

## Clustering

The KMeans algorithm is applied to cluster the preprocessed data based on extracted features. Nearest Neighbors (KNN) models are trained for each sensor value to predict the action and person for test data instances.

## Test Data Prediction

Test data instances are preprocessed similarly to the training data. For each test instance, the nearest neighbors in the training data are identified using the KNN models. Weighted voting is applied based on distances to determine the most likely action and person for each test instance.

## Generating Submission File

The predicted action and person for each test instance are compiled into a submission file with the corresponding IDs. The submission file is saved in CSV format for evaluation.

## Conclusion

This project demonstrates the application of unsupervised learning techniques, particularly KMeans clustering and KNN modeling, for predicting actions and persons from sensor data. By preprocessing the data and extracting relevant features, meaningful insights can be derived from the sensor data to make accurate predictions.

For detailed explanations of the code and implementation steps, refer to the provided code snippets and comments within the GitHub repository.
