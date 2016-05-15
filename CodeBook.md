### Introduction
This code book describes the variables, the data, and any transformations or work that you performed to clean up the data.

### Data Source
Original data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

According to the original source, the information for the data set is given below:
<i>"The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data."</i>

Description of the dataset here: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones


### Objective
R script run_analysis.R does the following:
1. Merge the training and the test sets to create one data set.
2. Extract only the measurements on the mean and standard deviation for each measurement.
3. Use descriptive activity names to name the activities in the data set
4. Label the data set with descriptive variable names.
5. From the data set in step 4, create a second, independent tidy data set with the average of each variable for each activity and each subject.


### run_analysis.R Implementation
Once the given data is loaded into into R, the following are the steps to transform the raw data into a tidy dataset:
<ol>
<li>Read the features and activity labels from separate files.</li>
<li>Select the variables to get mean and standard deviation of the data.</li>
<li>Generate test and train data and merge them to get the tidy data i.e. tidy_data.txt</li>
<li>Write the output cleaned data to a file with same name</li>
</ol>
