# Cyber-Attack-Detection-Using-MLP (Assignment)
Readme file:
1. CSTR_train_normal.mat: training input+output data under normal operation
CSTR_train_attack.mat: training input+output data under attack
CSTR_train_noise.mat: training input+output data under noisy measurement
2. CSTR_test_normal.mat: test input+output data under normal operation
CSTR_test_attack.mat:
test input+output data under attack
CSTR_test_noise.mat: test input+output data under noisy measurement
Note: each data file (.mat) is a data matrix, where the number of rows represents the number of
data samples, and the number of columns represents the number of time steps within each data
sequence + last column is the output label: 0-no attack, 1-attack)
(For example, CSTR_train_normal.mat contains 694*201 data points -- there're 694 data sequences,
where each data sequence includes 200 time steps (or called elements), and the last column = 0
represents no attack)
3. You should first load all the datasets into Matlab workspace using the following commands, and
then combine CSTR_train 'normal' and 'attack' together as one training dataset.
load('CSTR_train_normal.mat')
load('CSTR_train_attack.mat')
load('CSTR_train_noise.mat')
load('CSTR_test_normal.mat')
load('CSTR_test_attack.mat')
load('CSTR_test_noise.mat')
4. The first 200 columns in the combined training set should be treated as training input data, and
the last column should be treated as training output data.(For example, for classification between 'normal operation' and 'attack', the training input dataset
should be a matrix of 1388*200, and the training output data should be a matrix of 1388*1)
5. After importing the training input and output data into Neural Net Fitting toolbox, please pay
attention to the option ‘Matrix columns’ or ‘Matrix rows’. Refer to its description on the right, and
choose appropriately.
Remember: the number of rows in the data matrix represents the number of data samples, and the
number of columns represents the number of elements (i.e., time steps) within one data sample.
6. After you train the neural network model, please export the network to workspace, and test it on
testing dataset. Calculate how many testing samples are predicted accurately, and report the testing
accuracy.
