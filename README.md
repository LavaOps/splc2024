
# Additional data files for “Exploration of Failures in an sUAS Controller Software Product Line” - SPLC 2024

Each file is described in the readme below.

## Referencing this work
To reference this work please use the following paper:

@inproceedings{purandare:splc24,
author = {Purandare, Salil and Cohen, Myra B.},
title = {Exploration of Failures in an sUAS Controller Software Product Line},
year = {2024},
doi = {10.1145/3646548.3672597},
booktitle = {Proceedings of the 28th ACM International Systems and Software Product Line Conference},
pages = {125–135},
series = {SPLC '24}
}

## Paper link:  

https://dl.acm.org/doi/10.1145/3646548.3672597

# Feature Models

## feature_model_values.csv

This is the complete list of values for all parameters in our full feature model from RQ1 and RQ2. 
## large-model.xml
This is the feature model from FeatureIDE with 50 features (5 values each) based on the file feature_model_values.csv.
To open this in FeatureIDE, create a new project, rename this file 'model.xml' and replace the model.xml file created by the project with this file.

Due to limitations of the FeatureIDE tool naming conventions we have used the following conventions for naming the choices of features:
1. Becuase many of our values are repeated and repeat names are not supported, we have named each choice with its feature number (e.g. F#_) where the number is sequential based on the .csv file line number. For instance, the choices for the first feature start with F1_.
2. Since FeatureIDE at the time of this project did not support decimal points in names, we have replace all decimal points with underscores. For instance the value 0.35 is written as 0_35.  and if this is part of Feature 25 it would be: F25_0_35.  If there is no leading zero then the value is greater or equal to 1. For instance, F25_3_5 indicates this feature choice is 3.5.

## exhaustive_model.csv
This is the list of values for the smaller feature model which we explored exhaustively (RQ3)

## exhaustive_model.xml
This is the FeabureIDE model for smaller feature model with 8 features and 3 values each (RQ3)

To open this in FeatureIDE, create a new project, rename this file 'model.xml' and replace the model.xml file created by the project with this file.

Due to limitations of the FeatureIDE tool naming conventions we have used the following conventions for naming the choices of features:
1. Becuase many of our values are repeated and repeat names are not supported, we have named each choice with its feature number (e.g. F#_) where the number is sequential based on the .csv file line number. For instance, the choices for the first feature start with F1_.
2. Since FeatureIDE at the time of this project did not support decimal points in names, we have replace all decimal points with underscores. For instance the value 0.35 is written as 0_35.  and if this is part of Feature 25 it would be: F5_0_35.  If there is no leading zero then the value is greater or equal to 1. For instance, F5_3_5 indicates this feature choice is 3.5.

# Experimental Data
## 1-hop_complete.csv

This is the complete set of one-hop tests discussed in RQ1, including the configuration information as well as the mission and takeoff outcomes. 

## 1-hop_failure_reruns.csv

Each failure from the initial one-hop set was re-run four times, in order to verify that the original failing result was a true failure and not caused by external factors. This file contains all four reruns for each initially failing configuration. 

## 2-hop_complete.csv

This is the complete set of two-hop tests discussed in RQ2, consisting of 19,600 configurations. 

## 2-hop_failure_reruns.csv

Each failure from the initial two-hop set was re-run two times in order to verify the initial result. This re-run set consists of 26,511 total trials. 

## negative_interactions.csv

This sheet includes every negative interaction in the system between two individually passing parameter values. Configurations that are passing or include individually failure-inducing parameter values have been filtered out. 

## positive_interactions.csv

This sheet includes every positive interaction in the system that causes an individually failure-inducing parameter value to change its behavior when paired with another parameter. All failing configurations and individually succeeding pairs have been filtered out. 

## exhaustive_complete.csv

This is the complete set of results with the modified feature model for the exhaustive tests discussed in RQ3. 

## motivating_example_negative.ulg, motivating_example_positive.ulg

In our motivating example, we described a series of negative and positive interactions that caused unexpected flight behavior. These are ULog files from the missions discussed in that section. These flight logs contain configuration information as well as time series data. The flights can be replayed and analyzed using a tool like PX4 Flight Review (https://review.px4.io/) or parsed offline with a tool like Pyulog (https://github.com/PX4/pyulog). The flight review pages for the negative and positive interactions are also linked below. 

[Motivating Example: Negative Interaction](https://review.px4.io/plot_app?log=7b4efbff-fe4d-48b3-855d-34797ed27e8c "negative")

[Motivating Example: Positive Interaction](https://review.px4.io/plot_app?log=3c8ac916-5cf8-45e8-9c35-bc1736d7a0bc "positive")

## MotivatingExample.xml

This is the XML file for the feature model presented in the Motivating Example section. 
