=========================================================
* README file                                          *
=========================================================
* CS 7641 Project 1 - Supervised Learning (Spring 2017) *
=========================================================
* Prepared by: Franklin Onyekwum (fonyekwum3)           *
=========================================================
=========================================================



A.  SELECTED DATA SETS:
=======================
The 2 data sets I used are the Abalone dataset and the Wine Selection dataset. The datasets can be obtained via the following URLs:
 1. Download Abalone Dataset: http://archive.ics.uci.edu/ml/machine-learning-databases/abalone/abalone.data
 2. Download Wine Quality Dataset: http://archive.ics.uci.edu/ml/machine-learning-databases/wine-quality/winequality-white.csv 



B.  ANALYSIS METHODOLOGY USED:
==============================
All my analysis was performed using the WEKA GUI (version 3.8.1), which can be downloaded via the following URL:
 1. Download WEKA: http://www.cs.waikato.ac.nz/ml/weka/downloading.html
Furthermore, all analysis was carried out using the Explorer section of WEKA



C.  CONVERTING ORIGINAL ATTRIBUTE DELIMITERS FROM “;” TO “,”:
=============================================================
The datafile downloaded from UCI repository had semi-colon delimiters, instead ofcommas. 
For both datafiles this was corrected by opening the files in a text editor, and then finding and replacing the ‘;’ character with a ‘,’.



D.  CONVERTING .CSV DATAFILES TO .ARFF FORMAT:
==============================================
This was achieved for both datasets by loading the .csv files into WEKA, and then savin them as .ARFF files.



E.  SPLITTING DATA INTO TRAINING AND TEST SETS:
===============================================
Both datasets were split into a training set (70%) and a test set (30%) using the WEKA —> Filters —> Unsupervised -> Instance —> RemovePercentage filter, under the Filter section of the WEKA Preprocess tab.
After the required percentage was removed the training/test sets were saved.



F.  ATTRIBUTE SELECTION:
========================
 1. Abalone Dataset: All attributes were used here
 2. Wine Dataset: Attribute selection was performed by following these steps:
  a. Go to the Select Attribute tab in WEKA
  b. Select CfsSubSetEval from the Attribute Evaluator section (selected by default)
  c. Select GreedyStepwise from the Search Method section
  d. Select Cross-Validation (10-fold, Seed = 1) in the attribute Selection Mode section and Start the evaluator
  e. Select all attributes with num of folds(%) greater than or equal to 5.
The selected attributes for the wine dataset are volatile acidity, citric acid, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, and alcohol (and the quality output class).
All other attributes are then deleted from the training and test data sets.



G.  ONE-SHOT ENCODING:
======================
For the Wine data set, the nominal SEX attribute was converted to a numeric attribute, via manual one-shot encoding using MS Excel.



H.  CONVERSION OF OUTPUT ATTRIBUTES:
====================================
In both datasets, the output variable is originally numeric. They ere both converted to nominal attributes using the WEKA —> Filters —> Unsupervised -> Attribute —> NumericToNominal filter, under the Filter section of the WEKA Preprocess tab.



I.  HYPER-PARAMETER TUNING:
===========================
Some hyper-parameters were tuned manually, while other were tuned using grid-search (see Table 1 in the report document).
 1. Grid-Search parameter tuning in WEKA:
  a. On the Classify tab, select Meta —> CVParameterSelection from the Classifier section
  b. Click on the selected CVParameterSelector. This should bring up the GenericObjectEditor window.
  c. On the classifier line, choose the classifier for which you want to select hyper parameters (e.g J48, SMO,MultilayerPerceptron, etc).
  d. Click on the CVParameter text box. This should bring up the GenericArrayEditor window.
  f. Add each parameter that you want to tune using the grid search, in the following format: <parameter-letter> <starting-value> <ending-value> <step-size>
  g. Close the GenericArrayEditor, click OK on the GenericObjectEditor window, and start the classifier
  h. when the classifier is done running, the output window will display the optimal values of each added parameter.



J.  PERFORMING EXPERIMENTS:
==========================
All experiment (as described in the report) were performed in the Explorer segment of WEKA GUI.
Each classifier was selected from the Classifier section of the Classify tab, and configured by clicking on the selected classifier and entering any required attributes (see Table 1 in the report document for all attributes). 
