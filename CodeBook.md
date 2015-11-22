Code Book

Raw Data

The data was built from experiments conducted with 30 subjects between 19 and 48 years old.  Each person performed six activities: walking, walking upstairs, walking downstairs, sitting, standing, laying while wearing a smartphone. The embedded accelerometer and gyroscope captured signal measurements.

The measurement variables captured are the following:

•	mean: Mean
•	std: Standard Deviation
•	mad: Median Absolute Deviation
•	max: Largest Value in Array
•	min: Smallest Value in Array
•	sma: Signal Magnitude Area
•	energy: Energy Measure
•	iqr: Interquartile Range
•	entropy: Signal Entropy
•	arCoeff: Autoregression coefficients
•	correlation: Correlation Coefficient
•	maxinds: Index with the Largest Magnitude
•	meanFreq: Weighted average of the mean frequency components
•	skewness: Skewness of the frequency domain signal
•	kurtosis: Kurtosis of the frequency domain signal
•	bandsEnergy: Energy of the frequency interval
•	angle: Angle between vectors


Data Transformation

The raw data sets are processed using  the run_analysis.R script that creates the tidy data set.

Merge the training and test sets

The Features train and test data sets are merged: x_train, x_test
The Activity train and test data sets are merged: y_train, y_test
The Subject train and test data sets are merged: subject_train: subject_test

Extract the mean and standard deviation measurements

Only the values of the estimated mean (containing “mean”) and standard deviation (containing “std”) are retained.

Use descriptive activity names

The Six Activity labels are added as an additional column.

Label variables with descriptive names

The original variables were updated to be more descriptive as the following:

•	“t” replaced with “time”
•	“f” replaced with “freq”
•	Parentheses removed
•	Dashes removed
•	“std” changed to “StdDev”
•	“BodyBody” cleaned to “Body”
•	“Mag” updated to “Magnitude”
•	“Gyro” updated to “Gyroscope”
•	“Acc” updated to Acceler”

Create a tidy dataset
A final tidy data set is created where the measurements are averaged for each subject/activity combination.




