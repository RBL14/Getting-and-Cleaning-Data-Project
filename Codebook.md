###CODE BOOK

This file describes the variables, the data, and any transformations or work that I have performed to clean up the data.

The site where the data was obtained:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
The data for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

##Data Set Information

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. 
Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. 
Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. 
The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). 
The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity.
 The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.


##run_analysis.R

This R script performs the following steps, as per the project assignment instructions:

* Merges the training and the test sets to create one data set.
* Extracts only the measurements on the mean and standard deviation for each measurement.
* Uses descriptive activity names to name the activities in the data set
* Appropriately labels the data set with descriptive activity names.
* Creates a second, independent tidy data set with the average of each variable for each activity and each subject.


##variables

#Subject

experiment participant (id)

#Activity list

1. WALKING
2. WALKING_UPSTAIRS
3. WALKING_DOWNSTAIRS
4. SITTING
5. STANDING
6. LAYING

#Features list

Column numbers are extracted from the original data file, UCI HAR Dataset/features.txt

1.  TimeBodyAccelerometerMean()-X                     
2.  TimeBodyAccelerometerMean()-Y                     
3.  TimeBodyAccelerometerMean()-Z                     
4.  TimeBodyAccelerometerSTD()-X                      
5.  TimeBodyAccelerometerSTD()-Y                      
6.  TimeBodyAccelerometerSTD()-Z                      
7.  TimeGravityAccelerometerMean()-X                  
8.  TimeGravityAccelerometerMean()-Y                  
9.  TimeGravityAccelerometerMean()-Z                  
10.  TimeGravityAccelerometerSTD()-X                   
11.  TimeGravityAccelerometerSTD()-Y                   
12.  TimeGravityAccelerometerSTD()-Z                   
13.  TimeBodyAccelerometerJerkMean()-X                 
14.  TimeBodyAccelerometerJerkMean()-Y                 
15.  TimeBodyAccelerometerJerkMean()-Z                 
16.  TimeBodyAccelerometerJerkSTD()-X                  
17.  TimeBodyAccelerometerJerkSTD()-Y                  
18.  TimeBodyAccelerometerJerkSTD()-Z                  
19.  TimeBodyGyroscopeMean()-X                         
20.  TimeBodyGyroscopeMean()-Y                         
21.  TimeBodyGyroscopeMean()-Z                         
22.  TimeBodyGyroscopeSTD()-X                          
23.  TimeBodyGyroscopeSTD()-Y                          
24.  TimeBodyGyroscopeSTD()-Z                          
25.  TimeBodyGyroscopeJerkMean()-X                     
26.  TimeBodyGyroscopeJerkMean()-Y                     
27.  TimeBodyGyroscopeJerkMean()-Z                     
28.  TimeBodyGyroscopeJerkSTD()-X                      
29.  TimeBodyGyroscopeJerkSTD()-Y                      
30.  TimeBodyGyroscopeJerkSTD()-Z                      
31.  TimeBodyAccelerometerMagnitudeMean()              
32.  TimeBodyAccelerometerMagnitudeSTD()               
33.  TimeGravityAccelerometerMagnitudeMean()           
34.  TimeGravityAccelerometerMagnitudeSTD()            
35.  TimeBodyAccelerometerJerkMagnitudeMean()          
36.  TimeBodyAccelerometerJerkMagnitudeSTD()           
37.  TimeBodyGyroscopeMagnitudeMean()                  
38.  TimeBodyGyroscopeMagnitudeSTD()                   
39.  TimeBodyGyroscopeJerkMagnitudeMean()              
40.  TimeBodyGyroscopeJerkMagnitudeSTD()               
41.  FrequencyBodyAccelerometerMean()-X                
42.  FrequencyBodyAccelerometerMean()-Y                
43.  FrequencyBodyAccelerometerMean()-Z                
44.  FrequencyBodyAccelerometerSTD()-X                 
45.  FrequencyBodyAccelerometerSTD()-Y                 
46.  FrequencyBodyAccelerometerSTD()-Z                 
47.  FrequencyBodyAccelerometerMeanFreq()-X            
48.  FrequencyBodyAccelerometerMeanFreq()-Y            
49.  FrequencyBodyAccelerometerMeanFreq()-Z            
50.  FrequencyBodyAccelerometerJerkMean()-X            
51.  FrequencyBodyAccelerometerJerkMean()-Y            
52.  FrequencyBodyAccelerometerJerkMean()-Z            
53.  FrequencyBodyAccelerometerJerkSTD()-X             
54.  FrequencyBodyAccelerometerJerkSTD()-Y             
55.  FrequencyBodyAccelerometerJerkSTD()-Z             
56.  FrequencyBodyAccelerometerJerkMeanFreq()-X        
57.  FrequencyBodyAccelerometerJerkMeanFreq()-Y        
58.  FrequencyBodyAccelerometerJerkMeanFreq()-Z        
59.  FrequencyBodyGyroscopeMean()-X                    
60.  FrequencyBodyGyroscopeMean()-Y                    
61.  FrequencyBodyGyroscopeMean()-Z                    
62.  FrequencyBodyGyroscopeSTD()-X                     
63.  FrequencyBodyGyroscopeSTD()-Y                     
64.  FrequencyBodyGyroscopeSTD()-Z                     
65.  FrequencyBodyGyroscopeMeanFreq()-X                
66.  FrequencyBodyGyroscopeMeanFreq()-Y                
67.  FrequencyBodyGyroscopeMeanFreq()-Z                
68.  FrequencyBodyAccelerometerMagnitudeMean()         
69.  FrequencyBodyAccelerometerMagnitudeSTD()          
70.  FrequencyBodyAccelerometerMagnitudeMeanFreq()     
71.  FrequencyBodyAccelerometerJerkMagnitudeMean()     
72.  FrequencyBodyAccelerometerJerkMagnitudeSTD()      
73.  FrequencyBodyAccelerometerJerkMagnitudeMeanFreq() 
74.  FrequencyBodyGyroscopeMagnitudeMean()             
75.  FrequencyBodyGyroscopeMagnitudeSTD()              
76.  FrequencyBodyGyroscopeMagnitudeMeanFreq()         
77.  FrequencyBodyGyroscopeJerkMagnitudeMean()         
78.  FrequencyBodyGyroscopeJerkMagnitudeSTD()          
79.  FrequencyBodyGyroscopeJerkMagnitudeMeanFreq()     
80.  Angle(TimeBodyAccelerometerMean,Gravity)          
81.  Angle(TimeBodyAccelerometerJerkMean),GravityMean) 
82.  Angle(TimeBodyGyroscopeMean,GravityMean)          
83.  Angle(TimeBodyGyroscopeJerkMean,GravityMean)      
84.  Angle(X,GravityMean)                              
85.  Angle(Y,GravityMean)                              
86.  Angle(Z,GravityMean) 
