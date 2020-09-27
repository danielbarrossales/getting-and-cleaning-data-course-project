## Data
The data was taken from [UCI HAR Dataset](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)
The column names present in this project are:
1. SubjectId - Id of the subject;
2. ActivityId - Id of the activity;
3. ActivityLabel - Label of the activity;
4. Means and Standard Deviation from the following measurements:
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
## Transformations
A tidy data set was created with the average of each variable for each **activity** and each **subject**.
Abreviated names from columns were also changed for their extended names, for example: tBodyAcc became TimeBodyAcceleration
