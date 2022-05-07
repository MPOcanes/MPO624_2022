### HW/ take-home exam on Fourier module

0. **Why** would a sensible person decompose or expand their data series into a sum of harmonic (sinusoidal) functions? Hint: This is to make you read my "crashcourse" writeup. 

    - a. List some reasons why we might we expect or hope to find such signals in the atmosphere and ocean. Be sure to use both the words forced and free in your answer, and explain why harmonic forcing is expected. 

    - b. Explain the link between finding a statistically significant periodicity (a spectral peak) and predictability. 

1. What are the definitions and units of _wavelength_, _period_, _frequency_,  _wavenumber_, _amplitude_, _phase_? What does _monochromatic_ mean? 

2. For a discrete data series V(t) = {V<sub>i</sub>} with N values spaced dt apart, spanning the finite interval [0,T] with T = (N-1)dt, write down its Fourier decomposition: 

    a. Write it as a sum of cosine terms (with coefficients a0, a1, a2, a3...) and sine terms (with coefficients b1, b2, b3...), for the set of frequencies ω = {0,1,2,3...} times the lowest possible frequency or **fundamental harmonic** ω<sub>0</sub> = (2π/T). Follow equations 8.22-8.23 in the [Martinson book, p266](https://github.com/MPOcanes/MPO624-2020/blob/master/Course_Modules_Topics_Notebooks/series_analyses_and_FFT/Readings/Ch8_Martinson_proof.pdf). The lowest or fundamental frequency ω<sub>0</sub> is also called the **bandwidth**, since it discretizes the frequency domain into finite bins or bands (a good use for a bar graph). After the ... where you stop enumerating the many frequencies after 0,1,2,..., make your expression end with explicit terms at the **highest** possible frequency, called the **Nyquist** frequency. Why is there no b coefficient for zero frequency (b0=0)? Why does the Nyquist frequency also have only one coefficient? With these two special zeros, show that N is how many Fourier coefficients it takes to express this series of N values. 
    
    b. Write it again as a **discrete cosine transform**, using cosines only, but with phase offsets in each frequency (that is, with _amplitude A and phase φ_ rather than _sine and cosine_ components in each frequency). How are the A and φ coefficients related to a and b coefficients from part a? See Eq. (8.11) on p259 of the Martinson chapter linked above.  
    
    c. Write the complex version of the decomposition: V = ∑<sub>j</sub> c<sub>j</sub> exp(iω<sub>0</sub>t⋅j). Show how a<sub>j</sub> and b<sub>j</sub> relate to the real and imaginary parts of complex c<sub>j</sub>. This form is in [Wikipedia](https://en.wikipedia.org/wiki/Discrete_Fourier_transform). 
    
    d. Write the power spectrum P(ω) in terms of a and b coefficients; and also in terms of A and φ; and also in terms of the complex c. 

3. Suppose you have 100 years of tropical rainfall data at a point, one value per day, from a model. You want to ask if the model has the Madden-Julian oscillation, which Madden and Julian (1971) detected in nature: a statistically signifficant (above an AR1 red noise 'background' spectrum as a null hypothesis) spectral peak, _in the frequency band with 40-50 day periods_.  

    a. One simplest approach is to call numpy.fft() or scipy.periodogram() on the whole 100-year series. For this series with T = 100y and dt = 1d, **how many spectral power estimates fall in the 40-50 day band?** If you smooth the spectrum by averaging all these frequencies in the 40-50 day band together, your estimate for the power in this band with have twice that many degrees of freedom (DOFs), and won't have to be so extremely tall to pass the F-test. Remember, for just 2 DOFs like a raw [periodogram](https://en.wikipedia.org/wiki/Periodogram), the F-test requires a factor of 3 in variance for even an *expected or a priori* peak or trough to be 95% significant. 
    
    b. Another approach is to chop the series into segments, take the power spectrum of each segment, and then average those. **How short a segment will have exactly 1 power estimate in the 40-50 day frequency band?** How many such segments can you make from 100 years of data? Your power estimate in this spectral band will have twice that many degrees of freedom (DOFs). **How does that compare to your answer from a.?** Hopefully the same? 
    
    c. Now you want to test if the power in the 40-50 day band is "significanttly" higher than red noise (an AR1 autogressive "red noise", your **null hypothesis**, whose rejection would support the hypothesis that the MJO is a spectral peak). The test for comparing two variances by ratio is called the **F test**. Look it up and study its use (the end of Crashcourse document has a link). **For the DOFs from a. and b., how large a ratio of your actual power to the AR1 "null hypothesis" power would have p < 0.05 (95% significance level)?** 
    
    d. Suppose your data were not actually daily rainfall, but hourly rainfall amounts, subsampled once per day. If the variance of hourly rainfall is 5x bigger than the variance of daily rainfall, the extra 400% of variance will be misinterpreted as low frequencies, or **aliased** into the range of your spectrum (between the bandwidth and the Nyqyuist frequency), as my crashcourse notes explain. If you assume that this extra 400% of "aliased sampling noise" variance is distributed over your spectrum uniformly over the frequency bins, what is its effect on the F-test from c.? Discuss in sensible vocabulary terms; calculate something if you can.  
