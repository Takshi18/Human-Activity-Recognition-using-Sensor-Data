# A comparative study of different approaches to HAR using sensor data

Because of the various drawbacks of Machine learning models like feature engineering and all, we have a direct jump towards deep learninng models. The data for Human Activity Recognition(HAR) is going to be a time series data, thus models used are as follows-

1. LSTM (specialized RNN architecture)
2. CNN-GRU (a hybrid deep learning model)
3. Soft Attention mechanism (a basic attention model)

Here, two datasets have been used to do comparision between them - 
1. UCI-HAR
(available here https://archive.ics.uci.edu/dataset/364/smartphone+dataset+for+human+activity+recognition+har+in+ambient+assisted+living+aal)
  DATASET DESCRIPTION :
  1. How data was recorded ?
     30 participants (referred as subjects in this dataset) performed activities of daily living while carrying a waist-         mounted smartphone. The phone was configured to record two implemented sensors (accelerometer and gyroscope). For          these time series the directors of the underlying study performed feature generation and generated the dataset by          moving a fixed-width window of 2.56s over the series. Since the windows had 50% overlap the resulting points are 
      equally spaced (1.28s).This experiment was video recorded to label the data manually.

      By using the sensors(Gyroscope and accelerometer) in a smartphone, they have captured '3-axial linear 
      acceleration'(tAcc-XYZ) from accelerometer and '3-axial angular velocity' (tGyro-XYZ) from Gyroscope with several 
      variations.

       prefix 't' in those metrics denotes time.

      suffix 'XYZ' represents 3-axial signals in X , Y, and Z directions.

   2. How is the Data preprocessed?
      After getting Raw Sensor Data the Expert (Domain Expert, Signal Engineer Expert) are preprocessed this data and make        some useful feature. I am not expert but what I understand I explain here how these data are preprocessed.

      These sensor signals are preprocessed by applying noise filters and then sampled in fixed-width windows (sliding            windows) of 2.56 seconds each with 50% overlap. ie., each window has 128 readings.

      The accelertion signal was saperated into Body and Gravity acceleration signals(tBodyAcc-XYZ and tGravityAcc-XYZ)          using some low pass filter with corner frequecy of 0.3Hz.

      After that, the body linear acceleration and angular velocity were derived in time to obtian jerk signals           
      (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ).

      The magnitude of these 3-dimensional signals were calculated using the Euclidian norm. This magnitudes are     
      represented as features with names like tBodyAccMag_, tGravityAccMag, tBodyAccJerkMag, _tBodyGyroMag and 
      tBodyGyroJerkMag.

      Finally, We've got frequency domain signals from some of the available signals by applying a FFT (Fast Fourier       
      Transform). These signals obtained were labeled with prefix 'f' just like original signals with prefix 't'. These 
      signals are labeled as fBodyAcc-XYZ, fBodyGyroMag etc.,.

      These are the signals that we got so far.

      tBodyAcc-XYZ
      tGravityAcc-XYZ
      tBodyAccJerk-XYZ
      tBodyGyro-XYZ
      tBodyGyroJerk-XYZ
      tBodyAccMag
      tGravityAccMag
      tBodyAccJerkMag
      tBodyGyroMag
      tBodyGyroJerkMag
      fBodyAcc-XYZ
      fBodyAccJerk-XYZ
      fBodyGyro-XYZ
      fBodyAccMag
      fBodyAccJerkMag
      fBodyGyroMag
      fBodyGyroJerkMag

      We can esitmate some set of variables from the above signals. ie., We will estimate the following properties on each       and every signal that we recoreded so far.



      mean(): Mean value
      std(): Standard deviation
      mad(): Median absolute deviation
      max(): Largest value in array
      min(): Smallest value in array
      sma(): Signal magnitude area
      energy(): Energy measure. Sum of the squares divided by the number of values.
      iqr(): Interquartile range
      entropy(): Signal entropy
      arCoeff(): Autorregresion coefficients with Burg order equal to 4
      correlation(): correlation coefficient between two signals
      maxInds(): index of the frequency component with largest magnitude
      meanFreq(): Weighted average of the frequency components to obtain a mean frequency
      skewness(): skewness of the frequency domain signal
      kurtosis(): kurtosis of the frequency domain signal
      bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.
      angle(): Angle between to vectors.
      
      We can obtain some other vectors by taking the average of signals in a single window sample. These are used on the         angle() variable' `

gravityMean
tBodyAccMean
tBodyAccJerkMean
tBodyGyroMean
tBodyGyroJerkMean


    3. Y_Labels(Encoded)
      In the dataset, Y_labels are represented as numbers from 1 to 6 as their identifiers.
      WALKING as 1  
      WALKING_UPSTAIRS as 2
      WALKING_DOWNSTAIRS as 3
      SITTING as 4
      STANDING as 5
      LAYING as 6

      
      


4. WISDM dataset (available here - https://www.cis.fordham.edu/wisdm/dataset.php)

Codes are available at (sequentially)- 
1. Models applied on UCI-HAR Dataset
     a. At first various machine learning models have been applied on already feature engineered dataset             (dataset          is available     at provided link - folders named  - test and train)
     b. Then, we started with the Deep learning learning models 1-Layered LSTM then 2-Layered LSTM.
     c. Then, CNN-GRU has been applied on same dataset(UCI-HAR) in the file named - (CNN-GRU applied on UCI-HAR Dataset).
     d. After that, Soft attention mechanism has been applied on the file named - (Soft_Attention_mechanism on UCI-HAR)

2. Models applied on WISDM Dataset
   For this models, we have directly applied deep learning models on the raw data available in UCI-HAR dataset.
   a. Following the same sequence as above, all the mentioned models(LSTM,CNN-GRU,soft-attention mechanism) have applied         in          the file named - (Models applied on WISDM_Dataset).
     





