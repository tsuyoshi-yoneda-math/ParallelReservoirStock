Please acknowledge the use of these scripts in any publications that make use of them.

I developed a non-incremental online learning system using a parallelized reservoir and the corresponding data-driven filter. Unlike long-term learning models, its strength lies in its ability to adapt flexibly to sudden changes in patterns.

For the summary of parallelized reservoir, see

https://github.com/tsuyoshi-yoneda-math/SummaryNoteSlide-ML-Turbulence/blob/main/parallelized-reservoir.pdf

We applied this method to predict SP500 and the result is as follows:

<b>
Accuracy = 0.762,<br>
F1 = 0.712,<br>
Recall = 0.721.
</b>

<br><br>

Using the filtered data, along with a correlation of 0.985 between the filtered data and original data, is considered a fairly robust result.
The following is a comparable result from our study:

Gonzalo López Gil, Paul Duhamel-Sebline, Andrew McCarren,
An Evaluation of Deep Learning Models for Stock Market Trend Prediction
(2024) 

https://arxiv.org/pdf/2408.12408v1

Their result (using xLSTM-TS) is as follows:

Accuracy = 0.709,
F1 = 0.730,
Recall = 0.768.

If you want to know the mathematical structure of the data-driven filter, see the following paper:

``Long-term prediction of El Niño-Southern Oscillation using reservoir computing with data-driven realtime filter"

https://pubs.aip.org/aip/cha/article-abstract/35/5/053149/3347294/Long-term-prediction-of-El-Nino-Southern?redirectedFrom=fulltext
