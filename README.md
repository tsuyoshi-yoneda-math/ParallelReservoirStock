Please acknowledge the use of these scripts in any publications which make use of them.

I constructed non-incremental online learning of parallelized Reservoir (simple stock non-reduction model) and the corresponding data-driven filter (based on Bayesian optimization) for the parallel data.

The strong point of this learning scheme is that only the most recent 60 days of data are used to predict sp500 (strength of this model lies in its ability to flexibly adapt to sudden pattern change).
With this limited training data, online learning can be performed to predict whether the price of sp500 will rise or fall tomorrow.

Thirty trials were conducted, and the average was calculated. This can be considered a rolling window verification.

Since the evaluation covers multiple periods rather than a single period,
it eliminates concerns such as “Is the model only strong for a specific period?” or “Is it not just temporary overfitting or random bias?”.
By taking the average, it demonstrates that the model has consistent predictive power regardless of the period.

The result is as follows:

Accuracy = 0.762,
F1 = 0.712,
Recall = 0.721.

Using the filtered data, along with a correlation of 0.985 between the filtered data and original data, is considered a fairly robust result.
The following is a comparable result from our study:

An Evaluation of Deep Learning Models for Stock Market Trend Prediction
Authors: Gonzalo López Gil, Paul Duhamel-Sebline, Andrew McCarren
Year: 2024 

https://arxiv.org/pdf/2408.12408v1

Their result (using xLSTM-TS) is as follows:

Accuracy = 0.709,
F1 = 0.730,
Recall = 0.768.

If you want to know the mathematical structure of the data-driven filter, see the following paper:

``Long-term prediction of El Niño-Southern Oscillation using reservoir computing with data-driven realtime filter"

https://pubs.aip.org/aip/cha/article-abstract/35/5/053149/3347294/Long-term-prediction-of-El-Nino-Southern?redirectedFrom=fulltext
