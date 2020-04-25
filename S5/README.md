# Assignment - 5

# Experiment - 1 

Target:
Get the set-up right Set Transforms Set Data Loader Set Basic Working Code Set Basic Training & Test Loop

Results:
Parameters: 13,120 Best Training Accuracy: 99.30 Best Test Accuracy: 98.76

Analysis:
Good for a base model But far away from what we want to achieve

# Experiment - 2

Target:
Less than 15 epochs
Adding Batch Normalisation to improve accuracy & stabilisation
Results:
Parameters: 13,300
Best Training Accuracy: 99.80
Best Test Accuracy: 99.26
Analysis:
The accuracy has increased considerbaly but it looks like the model is overfitting
The number of parameter is still not under 10,000

# Experiment - 3


Target:
Less than 10000 parameters
Add Image Augmentation (Rotation)
Add GAP to reduce number of parameters
Restructure the architecture to meet receptive field requirement
Results:
Parameters: 9,174
Best Training Accuracy: 99.80
Best Test Accuracy: 99.48
Analysis:
The target accuracy is yet to be achieved
Looks like Image Augmentation has affected the model by a small percentage

# Experiment - 4


Target
Add LR Scheduler with a step LR of 0.5 after every 5 steps
Results
Number of Parameters = 9174
Best Train Accuracy = 99.22
Best Test Accuracy = 99.50
Analysis
Accuracy has improved very much
Next lets try applying dropout & also reducing the number of parameters

# Experiment - 5


Target
Test with Cyclic LR
Add small dropout of 4%
Results
Number of Parameters = 7758
Best Train Accuracy = 99.17
Best Test Accuracy = 99.45
Analysis
We have achieved the target of this execise, but theirs still room to experiment by increasing the dropout.
We have achieved greater Test accuracy in earlier experiments but they weren't consistent, so they we couldn't rely much on them.
