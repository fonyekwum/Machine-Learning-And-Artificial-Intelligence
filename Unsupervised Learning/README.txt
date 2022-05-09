======================================================================================

* README file                                  
*
=====================================================================================
* CS 7641 Project 3 - Unsupervised Learning and Dimensionality Reduction (Spring 2017) 
*
=====================================================================================

* Prepared by: Franklin Onyekwum (fonyekwum3)         
*
=========================================================
============================






A. DATA SETS USED:

==================
The 2 data sets I used are the Abalone dataset and the Wine Quality Selection dataset. The datasets can be obtained via the following URLs:
 
1. Download Abalone Dataset: http://archive.ics.uci.edu/ml/machine-learning-databases/abalone/abalone.data

 
2. Download Wine Quality Selection Dataset: http://archive.ics.uci.edu/ml/machine-learning-databases/wine-quality/winequality-white.csv 







B.  ANALYSIS METHODOLOGY USED:

==============================

All my analysis was performed using the WEKA GUI (version 3.8.1), which can be downloaded via the following URL:
 
1. Download WEKA: http://www.cs.waikato.ac.nz/ml/weka/downloading.html






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







F.  Downlaoding WEKA Add-ons:

=============================
 
1. StudentFilters: Contains the FastICA attribute selector, and can be downloaded va the WEKA Package Manager (WEKA GUI Chooser --> Tools --> Package Manager), or at https://github.com/cgearhart/students-filters/

2. XMeans: Can be downloaded via the WEKA Package Manager, or at http://weka.sourceforge.net/doc.packages/XMeans




G.  PERFORMING EXPERIMENTS:

===========================

All experiment (as described in the writeup document) were performed in the Explorer segment of WEKA GUI. Each classifier/clustering/attribute selection technique was selected from the Classify/Cluster/Select Attributes tab as required, and configured as required. 
All attributes were left at their default values, unless otherwise specified in the writeup document.




