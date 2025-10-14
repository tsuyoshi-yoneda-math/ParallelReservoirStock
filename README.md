Please acknowledge the use of these scripts in any publications which make use of them.

I constructed non-incremental online learning of parallelizable Reservoir (simple stock model). More precisely, I constructed non-incremental online learning of parallelized Reservoir (simple stock non-reduction model) and the corresponding realtime filter (based on Bayesian optimization) for the parallel data.

The strong point of this learning scheme is that only the most recent 60 days of data are used to predict sp500 (strength of this model lies in its ability to flexibly adapt to sudden pattern change).
With this limited training data, online learning can be performed to predict whether the price of sp500 will rise or fall tomorrow.


Thirty trials were conducted, and the average was calculated. This can be considered a rolling window verification.

Since the evaluation covers multiple periods rather than a single period,
it eliminates concerns such as “Is the model only strong for a specific period?” or “Is it not just temporary overfitting or random bias?”.
By taking the average, it demonstrates that the model has consistent predictive power regardless of the period.

Accuracy = 0.762
F1 = 0.712
Recall = 0.721

The following is a comparable result from our study:

An Evaluation of Deep Learning Models for Stock Market Trend Prediction
Authors: Gonzalo López Gil, Paul Duhamel-Sebline, Andrew McCarren
Year: 2024 
https://arxiv.org/pdf/2408.12408v1

This can be concluded as a fairly robust result.


To make the comparison among filters more meaningful, the correlation with the raw data can be used as a reference indicator alongside accuracy and F1.
