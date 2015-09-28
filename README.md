# TidyDataAssignment

Codebook.md


the raw data was made available from a Web sight research on HumanActivityRecognition Research using Samsung Smartphones.

The experiment consisted of 30 Volunteers between 19-48 engaging in 1 of 6 activities while sensors are active. (Walking,Walking upstairs, Walking downstairs, Sitting, Standing, and Laying)

There was some initial filtering of the raw data done on the raw data by the experimenters as detailed in the ReadMe.txt and Features included with the raw data.
The filtering was in summary primarily to distinguish jerk and human motion from gravitational interference with the Accelerom. and other noise.

Additionally, other data was extrapolated by calculation to extrapolate magnituded of various aspects of the data and derive some extended factors.

The 30 subjects were divided 30/70 to test/train groups arbitrarily and data was gathered through the aforementioned instruments at the described sample rate.

that data in its raw form was then used to gather various categories of information such as mean, standard deviation, median and other analysis.

My object, was to get a tidydataset subset with the mean and standard deviation for each category of consideration per subject and per Activity.

I started out by gathering the relevant data for both train and test sets and attaching them to their respective subjects while corresponding to each activity in turn.

that was done by two iterations of the SAIndex() function, one for each group(train and test).
Having Corresponded Activities and Subjects with their raw data, I proceeded to get the features list made available to link the columns of data with their value names to derive what the numbers corresponded to.. the NamingColumns() function.

Once that is together, the two disparate datasets are rebound together and Activity names are introduced in the fields instead of their corresponding numbers.

All the data clean up is done with two steps, once all the code is in the workspace.

the first step to get to Step 4 of the Assignment before the final TidyData. That is the WHOLE dataset, is arrived by calling the function Merge() with arguments, as long as one is in the main Raw Dataset folder downloaded.
plyr, and dplyr, are used so those packages must be present in the global workspace for these functions not to give an error.

With that in place, Merge() will return a tidy WHOLE dataset.

then the result of that could be sent as an argument to NewTidySet([result of Merge])to get the final Tidydataset of step 5 as explained.. 

The result is a TidyDataSet of 73 columns, each corresponding to and labeled as, respective mean and st deviation data from the various sensor derivations in the raw data taken (from the two tri-axial sensors and analyzed as made available in the raw data) as mean of each individual numbered 1-30 under subject and secondly, means taken corresponded cross individual by activity which are listed as 1-6.

the steps taken in the functions is layed out in detail with comments.

thank you
