Getting-Cleaning-Data Course Project

This readme document describes step by step how to prepare and clean the dataset presented in the Course Project.

Unzip the source file with the data in a local directory of your machine (you can find the zip file here: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip).

Copy the "run_analysis.R" script in your R working directory.

Make sure that all the files your are going to read from the unzipped folder, are placed in your working directory.

features.txt
activity_labels.txt
X_train.txt
subject_train.txt
y_train.txt
X_test.txt
subject_test.txt
y_test.txt
Run the "run_analysis.R" script.
The main steps performed in the "run_analysis.R" script have been the following:

Reading data from each single .txt file using the read.table command
Merge train data horizontally with its corrspondent subject and activity columns, using cbind function. Do the same with test data.
Merge train and test data vertically using the rbind function.
Assign activity_num to their correspondent activity_type values using a lookup table, and finally add the activity_type column to the merged data set
Subset only measurement of the mean and standard deviation
Create a new idependent data set with the average of each variable for each activity and each subject, using the aggregate function.
Write the resulting data set into a .txt file names "tidy_dataset_with_avg.txt".