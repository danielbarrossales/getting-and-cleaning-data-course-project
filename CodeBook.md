## Data
The data was taken from [UCI HAR Dataset](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)
The column names present in this project are:
1. subject - Id of the subject;
2. activity - Id of the activity;
3. Means and Standard Deviation from the following measurements:
      * tBodyAcc-XYZ
      * tGravityAcc-XYZ
      * tBodyAccJerk-XYZ
      * tBodyGyro-XYZ
      * tBodyGyroJerk-XYZ
      * tBodyAccMag
      * tGravityAccMag
      * tBodyAccJerkMag
      * tBodyGyroMag
      * tBodyGyroJerkMag
      * fBodyAcc-XYZ
      * fBodyAccJerk-XYZ
      * fBodyGyro-XYZ
      * fBodyAccMag
      * fBodyAccJerkMag
      * fBodyGyroMag
      * fBodyGyroJerkMag

According to the UCI HAR Dataset the features of the data was retrieved as following: 
- "The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz"; 
- "Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag)"; 
- "Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals).".
## Transformations
- The original data set provides several files divided in a train and test datasets, this script merged both datasets and files into a single unified dataset;
- Abreviated column names were written in full, for example: "fBodyAccMag" becomes "FrequencyBodyAccelerationMagnetude";
- activity and subject were named as ActivityId and SubjectId;
- A new column was added with the label for each activity:
     - 1 => WALKING;
     - 2 => WALKING_UPSTAIRS;
     - 3 => WALKING_DOWNSTAIRS;
     - 4 => SITTING;
     - 5 => STANDING;
     - 6 => LAYING.
 - A final data set was created with the average of each variable for each **ActivityId** and each **SubjectId**

A tidy data set was created with the average of each variable for each **activity** and each **subject**.
Abreviated names from columns were also changed for their extended names, for example: tBodyAcc became TimeBodyAcceleration
