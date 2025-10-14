Please acknowledge the use of these scripts in any publications which make use of them.

I constructed non-incremental online learning of parallelizable Reservoir (simple stock model).

The strong point of this learning scheme is that only the most recent 60 days of data are used to predict sp500 (strength of this model lies in its ability to flexibly adapt to sudden pattern change).
With this limited training data, online learning can be performed to predict whether the price of sp500 will rise or fall tomorrow using only information from the past four days.
A lag is incorporated, making it a practical setting for actual use. 
By incorporating a lag, it might be possible to reduce the impact of short-term noise on the results.

Thirty trials were conducted with a one-day shift, and the average was calculated. This can be considered a rolling window verification.

Since the evaluation covers multiple periods rather than a single period,
it eliminates concerns such as “Is the model only strong for a specific period?” or “Is it not just temporary overfitting or random bias?”.
By taking the average, it demonstrates that the model has consistent predictive power regardless of the period.

Accuracy = 0.576

This is significantly better than random ≈ 0.50 and always predicting “up” ≈ 0.53–0.55.


F1 = 0.585
→ The precision/recall balance is also reasonable.

Recall = 0.676
→ There is a strong tendency not to miss upward movements (which is advantageous from an investment strategy perspective).

Considering the constraint of using only information from the past four days, this can be concluded as a fairly robust result.


To make the comparison among filters more meaningful,
the correlation with the raw data can be used as a reference indicator alongside accuracy and F1.
