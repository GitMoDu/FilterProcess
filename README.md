# IFilter

A collection of, Arduino compatible, signal processing filters, collections and process task to update values.

Input/Output is 16 bit wide [ 0 : 65535].

FilterGroup - Template class to generate a filter collection, which is added one by one in setup/runtime.

FilterProcess - Useful to scheduled asynchronous filter step updating, for a FilterGroup.

IFilter - Common interface to all filters and base class for new filters.



Available filters:

EMA (Exponential Moving Average) - Optimized for integer operations. Inspired by https://www.norwegiancreations.com/2016/08/double-exponential-moving-average-filter-speeding-up-the-ema/ .

![](https://raw.githubusercontent.com/GitMoDu/IFilter/master/Media/ResponseEMA.png)

TemporalOversamplingFilter - Useful to get 16 bits out of a 8 bit signal, by oversampling temporaly and performing a weighted average for the result, tending to the freshest values to reduce latency.
