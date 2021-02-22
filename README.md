# RUL_Prediction_for_predictive_maintenance

Predictive Maintenance is used to determine the condition of an equipment to plan the maintenance/failure ahead of its time. one of the most used techniques in PdM is the calculating Remaining useful life (RUL) which is the length of time a machine is likely to operate before it requires repair or replacement. By taking RUL into account, engineers can schedule maintenance, optimize operating efficiency, and avoid unplanned downtime. For this reason, the objective of this project is to implement a machine learning models combined with reliability engineering tools such as exponential degradation model to fit time series models to condition indicators extracted from sensor data and then predict when the condition indicator will cross the threshold


# Data

Data sets consist of multiple multivariate time series. Each data set is further divided into training and test subsets. Each time series is from a different engine – i.e., the data can be considered to be from a fleet of engines of the same type (https://data.nasa.gov/dataset/Turbofan-engine-degradation-simulation-data-set/vrks-gjie). Each engine starts with different degrees of initial wear and manufacturing variation which is unknown to the user. This wear and variation is considered normal, i.e., it is not considered a fault condition. There are three operational settings that have a substantial effect on engine performance. These settings are also included in the data. The data are contaminated with sensor noise.

The engine is operating normally at the start of each time series, and starts to degrade at some point during the series. In the training set, the degradation grows in magnitude until a predefined threshold is reached beyond which it is not preferable to operate the engine. In the test set, the time series ends some time prior to complete degradation. The objective of this project is to predict the number of remaining operational cycles before in the test set, i.e., the number of operational cycles after the last cycle that the engine will continue to operate properly. the dataset provided by NASA contains three types of files :

1.	train_FD001.txt (Training data) --> It is the aircraft engine run-to-failure data.
2.	test_FD001.txt(Testing data) --> It is the aircraft engine operating data without failure events recorded.
3.	RUL_FD001.txt(Ground truth data) --> It contains the information of true remaining cycles for each engine in the testing data.


The data are provided in a txt format with 26 columns of numbers, separated by spaces. Each row is a snapshot of data taken during a single operational cycle; each column is a different variable. The columns correspond to:

- unit number
- time, in cycles
- operational setting 1
- operational setting 2
- operational setting 3
- sensor measurement 1
- sensor measurement 2
- ...
- sensor measurement 26

# References
A. Saxena, K. Goebel, D. Simon, and N. Eklund, “Damage Propagation Modeling for Aircraft Engine Run-to-Failure Simulation”, in the Proceedings of the 1st International Conference on Prognostics and Health Management (PHM08), Denver CO, Oct 2008.

A. Saxena and K. Goebel (2008). "Turbofan Engine Degradation Simulation Data Set", https://ti.arc.nasa.gov/c/13/), NASA Ames, Moffett Field, CA."
