# Codebook

Original data and description from [here](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) [1].

## Experiment

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details.

## Data

### `tidy_data.txt`

This data set contains one row per observation, consisting of:

 * `subject` -- the ID of the subject under measurement; integer between 1 and 30.
 
 * `activity` -- the activity during which the measurement was taken;
     one of `Laying`, `Sitting`, `Standing`, `Walking`, `Walking_downstairs`, and
     `Walking_upstairs`.
     
 * 66 measurement columns documented in the original file `features_info.txt`.
    
    * Names translate as 
        
            Time      -> t
            Frequency -> f
            Acceleration -> Acc
            Magnitude    -> Mag
            Mean         -> -mean()-
            Std          -> -std()-
             
    * Measurements of `Acceleration` are in unit g, normalized to [-1,1].
    * Measurements of `Gyro` are in unit radians/s, normalized to [-1,1].

### `tidy_avg_data.txt`

This data set contains averages of all variables mentioned above 
for each pair of subject and activity; 
names are prefixed with `Avg` to indicate this.

Units and ranges remain the same.

---

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012
