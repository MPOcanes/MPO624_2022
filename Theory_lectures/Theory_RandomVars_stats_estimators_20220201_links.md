# Theory about [random variables](https://en.wikipedia.org/wiki/Random_variable)

## [Probability distribution](https://en.wikipedia.org/wiki/Probability_distribution) (PD, discrete) and density function (PDF, continuous) 

PD or PDF values have TWO properties: 

1. They are nonnegative
2. They sum (PD) or integrate (PDF) to unity. <-- (1 with no units!)

Property 2 implies that a PDF = d(unity)/d(*variable*) has **units: inverse of *variable* units** 

## PDF and CDF

    - the median is halfway up the CDF
    - a mode is the a maximum of a PDF
    

## [Statistical inference](https://en.wikipedia.org/wiki/Statistical_inference): estimating a *population* parameter from a *sample* 

*Representativeness* of the sample is a huge, upstream (sometimes hidden) issue. Viewed the other way, one's result applies to only a *sub-population*, a caveat one must clearly understand and report. **Brains on, my students!**  

## [Statistic](https://en.wikipedia.org/wiki/Statistics): broad term for any measure of some attribute of a sample

Some statistics are good-faith *estimates* (the result produced by an *estimator*) of something scientific -- like the probability your pet idea is wrong! Others are merely *characterizations* of a set of numbers (possibly meaningless or misleading! but often useful for *exploration* of a dataset). 

**Explore first, exploit (estimate) later!** Data need to be checked visually. 

## [Estimator](https://en.wikipedia.org/wiki/Estimator): a statistic that represents an *interpretation*

Probability is the meaning or interpretation of SOME statistics; statistics is ALL the arithmetical operations we can do on data (meaningful or not!). 

There are many, sometimes competing, virtues to estimators: 

    - ["Unbiased"](https://en.wikipedia.org/wiki/Bias_of_an_estimator): an estimator that, if applied many times and averaged, gives the correct **expectation value** or **mean**.

    - ["Maximum Likelihood"](https://en.wikipedia.org/wiki/Maximum_likelihood_estimation): a popular estimator in theory, because maximizing a function is easy: set the first derivative to zero (and if necessary, second derivative <0) and solve. It corresponds to the **mode** of a distribution. Can be biased: **The maximum likelihood of hourly rainfall is zero, but sometimes rain happens and that matters!**
    
    - ["Robust"](https://en.wikipedia.org/wiki/Robust_statistics): a safe estimator, one that is not too affected by outliers. For instance the **median** house price as a measure of typical is not affected by sale of a few super-mansions, unlike the **mean**. 
    
    - ["Efficient"](https://en.wikipedia.org/wiki/Efficiency_(statistics)): an estimator that converges on the correct value quickly for even small sample sizes.