# TFM
Files used for my Masters thesis.

This repository contains the scripts and documentation created during my studies for my Master's thesis.

Original Title: "Uso de machine learning en la determinación de niveles de suciedad en sistemas fotovoltaicos a partir de paramentos ambientales"
Author: Luiza Araujo Costa Silva
Oriented by: Profª. Drª. María del Carmen Pegalajar Jiménez
Universidad de Granada

Translated title: Use of machine learning on the determination of soiling in photovoltaic systems through environmental parameters

# ABSTRACT

The constant and actual urban and industrial growth of our society also rises the demand for more renewable sources of energy. 
One of the biggest bets on clean energy sources is photovoltaic energy (PV) which is generated from solar light on photovoltaic solar panels.

However, many factors impact the PV power capacity. One of these, known as soiling, is the dirt that naturally settles over FV panels due to atmospheric and meteorological events. 
The measure of soiling level is known as Soiling Ratio, or simply “SR”. Many mathematical models are used to estimate power losses by soiling.

Using data of environmental parameters from satellites and SR measured in a soiling station in Jaén (Spain), this study proposes to build machine learning models to predict soiling based on the time series data of these measurements. 
As so, the achieved metrics are evaluated and compared to the ones achieved by the mathematical models currently used.

The acquired data is split in 3 different inputs, together with sliding windows (the measured SR of previous days): 
1) features selected by Boruta algorithm, 
2) features used on the mathematical models and 
3) only sliding windows.

To each of these inputs five regression methods were applied: Linear Regression, Decision Tree, Random Forest, Multi-layer Perceptron and LSTM. 
Through the experimentations many hyperparameters were tested.

After the experiments, an analysis of the results is presented to each one of the inputs and algorithms. 
Furthermore, when analyzing all experiments, it is stated that the Linear Regression and the MLP with 1 hidden layer and 30 neurons models have the best results to the proposed problem. 

Finally, these two best models are used to make sequential predictions. 
Meaning, the output of previous days predictions is used as input for future predictions. 
Both predictors present similar and great results, with an ability to predict until 5 future days with low RMSE (0.002 in average). 
Even the larger term predictions have satisfactory outcomes: RMSE of 0.0014 on the prediction of 90 days ahead, comparing to the 0.026 average error obtained with the mathematical models.

In addition, it could not be confirmed if the best results are obtained without the use of environmental parameters because of the fact that satellite data are more susceptible to errors, o if they actually became noise to the predictor, for been external data to the time series. 
Further research is needed to certify their influence in the results.

Keywords: machine learning, artificial neural network, linear regression, MLP, soiling, environmental parameters, photovoltaic. 
