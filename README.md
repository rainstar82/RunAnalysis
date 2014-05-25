RunAnalysis
===========
Getting and Cleaning Data Course Project Code Book 
Anahita Saghafi 25/05/2014

Steps

1. Set working directory and check it
setwd("C:\\Users\\anahitas\\Documents\\coursera\\Getting and Cleaning Data\\getdata-projectfiles-UCI HAR Dataset\\UCI HAR Dataset")
getwd()

2. Read "features.txt" and save as "Featutes" with column names "FeatureId and FeatureName" ## 561 obs. of 2 variables

3. Read test set data(X_test.txt), and use FeatureName for column names ## 2947 obs. of 561 variables

4. Read test activity labels (y_test.txt) and use "ActivityLabelID " for column names

5. Read test subjects (subject_test.txt) and use SubjectID for column names
 
6. Read train set  data(X_train.txt), and use FeatureName for column names ## 7352 obs. of 561 variables
 
7. Read train activity labels (y_train.txt) and use "ActivityLabelID " for column names
 
8. Read train subjects (subject_train.txt) and use SubjectID for column names
 
9. Perform rbind to testData and trainData to create mergedSetData ## 10299 obs of 561 variables

10. Perform rbind to testActivityLabels and trainActiviyLabels to create mergedSetActivityLabels   
 
11. Perform rbind to testSubjects and trainSubjects to create mergedSetSubjects   

12. Read activity labels (activity_labels.tct) and use "ActvityLabelID" and "ActivityLabelName" for column names   
 
13. Replace activity label ids with activity label names and call it ActivityLabelName  

14. Get subset of features related to mean and std and apply to the mergedSetData to get mergedSubsetData  

15. Add activity label names (ActivityLabelName) and subject id (SubjectID) to the merged sub    

16. Finally write clean data with descriptive activity  names into mergedSubsetData.txt ##10299 obs. of 68 variables

17. Use library data.tabe to create a data table megedSubsetDataTable
 
18.  Create mergedSubsetDataTable from mergedSubsetData
 
19. Use columns SubjectID and ActivilityLabelNames of mergedSubsetDataTable to create average data
 
20. OrderAverageMegedSubsetData by SubjectIDs ##180 obs. of 68 variables

21. Write the second data set "AverageMegedSubsetData" to complete the course project.
## 10299 obs. of 68 variables


==================================================================
Reference Data Set:
[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

==================================================================
Reference: 

==================================================================
Human Activity Recognition Using Smartphones Dataset
Version 1.0
==================================================================
Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
Smartlab - Non Linear Complex Systems Laboratory
DITEN - Università degli Studi di Genova.
Via Opera Pia 11A, I-16145, Genoa, Italy.
activityrecognition@smartlab.ws
www.smartlab.ws
==================================================================

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 



The dataset includes the following files:
=========================================

- 'README.txt'

- 'features_info.txt': Shows information about the variables used on the feature vector.

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

The following files are available for the train and test data. Their descriptions are equivalent. 

- 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

- 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis. 

- 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration. 

- 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second. 

Notes: 
======
- Features are normalized and bounded within [-1,1].
- Each feature vector is a row on the text file.

For more information about this dataset contact: activityrecognition@smartlab.ws

License:
========
Use of this dataset in publications must be acknowledged by referencing the following publication [1] 

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.

Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.

