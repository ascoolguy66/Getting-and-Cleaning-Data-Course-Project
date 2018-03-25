## Code Book for Course Project

### Overview

[Source](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) of the original data:

	https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

[Full Description](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) at the site where the data was obtained:

	http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
	
### Process

The script `run_analysis.R` performs the following process to clean up the data
and create tiny data sets:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names.
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

### Variables

- S - Subjects. Combined data set of the two above variables.
- features - Names of for data columns derived from featuresList
- keepColumns - logical vector of which features to use in tidy data set
- tidyData - subsetted, human-readable data ready for output according to
  project description.
- uS - unique subjects from S
- nS - number of unique subjects
- nA - number of activities
- nC - number of columns in tidyData
- td - second tiny data set with average of each variable for each activity and
  subject

### Output

#### tidyData.txt

`tidyData.txt` is a 10299x68 data frame.

- The first column contains subject IDs.
- The second column contains activity names.
- The last 66 columns are measurements.
- Subject IDs are integers between 1 and 30.
