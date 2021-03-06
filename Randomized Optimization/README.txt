=============================================================
* README file                                               *
=============================================================
* CS 7641 Project 2 - Randomized Optimization (Spring 2017) *
=============================================================
* Prepared by: Franklin Onyekwum (fonyekwum3)               *
=============================================================
=============================================================



A.  SELECTED DATA SET FOR NEURAL NETWORK:
=========================================
The data set I used is the UCI White Wine classification dataset. 

The dataset was previously pre-processed to select relevant attributes and also normalized, as described in the README.txt file for Assignment 1.

The pre-processed and normalized dataset is located in the the included ABAGAIL library, at “ABAGAIL/src/exp/WhiteWine/wineequality-white.csv”



B.  ANALYSIS METHODOLOGY USED:
==============================
All my analysis was performed using the ABAGAIL Library. However, since I made various modifications to the standard ABAGAIL library, I have included a version of the library that contains my modifications



C.  SETTING UP ABAGAIL:
=======================
To set up the included ABAGAIL library for use with Eclipse, please follow the set up instructions at  http://abagail.readthedocs.io/en/latest/faq.html#user-content-how-to-use-abagail-with-eclipse 



D.  GENERATING DATA FOR VARIOUS ANALYSIS:
=========================================
All of the data used for analysis in the report can be generated by performing the following actions:

1. Investigation of algorithms performance when training neural network with varying number of epochs/iterations: Run the WhiteWine.java class, located at “ABAGAIL/src/WhiteWine.java“ or in the default package in Eclipse.

2. Generate learning curves for algorithms for training neural network: Run the WhiteWine2.java class located at “ABAGAIL/src/WhiteWine2.java” or in the default package in Eclipse.

3. Generate data for Knapsack Problem: Run the KnapsackTest.java class, located at “ABAGAIL/src/opt/test/KnapsackTest.java” or in the opt.test package in Eclipse.

4. Generate data for Traveling Salesman Problem: Run the TravelingSalesmanTest.java class, located at “ABAGAIL/src/opt/test/TravelingSalesmanTest.java” or in the opt.test package in Eclipse.

5. Generate data for Continuous Peaks Problem: Run the ContinuousPeaksTest.java class, located at “ABAGAIL/src/opt/test/ContinuousPeaksTest.java” or in the opt.test package in Eclipse.


