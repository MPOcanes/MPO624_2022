# Syllabus of MPO/ATM 642, spring 2020
Applied Data Analysis (ADA) in an ocean/atmosphere context. 

Instructor: Brian Mapes, mapes@miami.edu. MSC366 is my office. 

Class meets: 10:30-11:45 Tues-Thurs

Clinic / office hours: By arrangement

No required text, all software is free. Supplemental readings may be found in the Readings area. 

## Goals and spirit of the course
##### _If you want to build a ship, don't drum up people to collect wood and don't assign them tasks and work, but rather teach them to long for the endless immensity of the sea. --Antoine de Saint-Exupery_

Learning outcomes: 

  (1) an appreciation, deep interest, appropriate level of confidence, and positive feeling for lifelong learning about ADA and evidence based reasoning: the essence of the life of the mind

  (2) a broad vocabulary about the space of data analysis concepts and tools, from probability (frequentist and Bayesian) to standard statistics (correlation and regression; parametric hypothesis testing and 'significance') to emerging methods (information theory and compression, nonparametric methods including machine learning)

  (3) software skills: a can-do feeling about accessing and understanding the exploding universe of computational tools
  
  (4) a personal success at expert depth in some technique and application (your project)

## Activities and grading
We have 28 75-minute classes together, plus double that much of your time dedicated to working on your own (or with me or the TA in office hours/ ‘clinic’ sessions). I will try to respect student time by bounding the assignments according to ability levels. Earnest effort at this time level will suffice for success, even as there is always more to know. Collaboration among students is strongly encouraged, within the [UM graduate honor code](https://www.grad.miami.edu/_assets/pdf/graduate_student_honor_code_2016_2017.pdf). 

### Grading weights are: 
  * 30% Attendance and participation in class. 
  
  * 40% Homework assignments and perhaps one in-class exam.
    
  * 30% End-of term research project presentation.
  
  
## Course structure

### 3 modules: basic concepts & notation, empirical methods, traditional analyses

1. Notations & concepts. What is science, what is evidence?

  - Notations: Numbers +/- uncertainty. Sets. Means and deviations. Random variables. Functions. Series and sequences. Matrix algebra. Convolution. Probability notation. Correlation, covariance, and regression. Causality graphs. Flowcharts and workflows. Discrete vs. continuous notations (sum vs. integral, difference vs. derivative). 

  - Concepts and vocabulary: Systems and boundaries. Signal and noise. Independence and orthogonality. Joint, marginal, conditional. Optimization and estimation. Screening and filtering. Information content, compression, and degrees of freedom. Monte Carlo ideas: resampling, synthetic data. 
  
  - Dichotomies: frequentist vs. Bayesian probability; paramatric vs. nonparametric statistics; unbiased vs. maximum-likelihood estimators; a priori vs. a posteriori significance; overfitting vs. underfitting; hypothesis vs. null hypothesis.
  
  - Strengths and virtues: Fit for purpose. Informative. Valid. Simple. Unbiased. Efficient. Accurate. Faithful. Optimal. Likely. Plausible. Improved. Robust. Reliable. Safe. Empirically adequate. Resolving power. Predictive power. 

2. Empirical or data-driven analysis and its pitfalls (overfitting, underfitting). Machine learning. Maximum Covariance techniques: `data(x,t) = EOF1(x) PC1(t) + EOF2(x) PC2(t) + … `  

3. Series methods for data ordered along a dimension (time series). Fourier mapping to/from spectral space. Common null hypotheses (white and colored noises, especially AR1 “red noise”). A glimpse of wavelet methods. 



## Provisional schedule: 

week | Tuesdays theory | Thursdays computers | dates
-----|----------|-----------|------
1 | Assignment: Create a [hypothes.is](https://web.hypothes.is/start/) account and install their Chrome plugin. Now, create some annotations on these **3 readings: 1.** [**What is science?**](https://www.nap.edu/read/13163/chapter/4) *Close the paywall overlay if it pops up, the text is free behind it.* Read the whole article and opine on what it says. See anything surprising or interesting or debatable? **2.** [**p-values explained simply**](https://towardsdatascience.com/p-value-explained-simply-for-data-scientists-4c0cd7044f14). Did you know this? Have any questions? Any debates? Do you see my one little annotation there? **3. An open-source research paper of your choosing.** Focus your attention and comments on the *experience of the key quantitative evidence (table, graph, image), **not** on the content of the scientific claims.* Specifically, what is the clinching observation *that the reader makes on the page?* A number is different from zero? A number is big, or great, or small, or greatly negative? A curve or pattern is seen to be clearly similar to another one, or clearly different from it? Is a statistical test used (like a p-value)? Share your level of understanding of the evidence (whether clear or confused), and share your course goals to learn to create or better understand such evidentiary artifacts. | Computer & github & Jupyter setup and orientation   |

See CALENDAR.md for further detail
