Project 1: Statistics - Stroop Effect
====================
##### Author: Nikolas Thorun

#### Introduction:

The Stroop effect is a demonstration of cognitive interference where a delay in the reaction time of a task occurs due to a mismatch in stimuli. When a word such as blue, green, red, etc. is printed in a color differing from the color expressed by the word's semantic meaning (e.g. the word "red" printed in blue ink), naming the color of the word takes longer and is more prone to errors than when the meaning of the word is congruent with its ink color.
For this project, this author received two sets of data with people's reaction times. One dataset contains the times for the congruent test, that is, color names that correspond to the ink of the words and the other data set contains the times for the incongruent test.


##### What is the independent variable? What is the dependent variable?

The independent variable is the condition of congruence (whether words are congruent with colors or not). The dependent variable is the individual's response time, as it varies according to the congruence condition.

Defining the hipothesis:

 ![hipothesis](hipothesis.png "Hipothesis")

##### What would be an appropriate set of hypotheses for this task? What kind of statistical test do you expect to perform? Justify your choices.

Is the average response time of individuals to the two tests very different? That is, with a given alpha level, will we reject the null or not?

The statistical test expected to perform this task is the _t-test,_ as we do not know the mean and standard deviation of the population and, in addition, the sample size is small `(n <30)`, making it impossible to use the _z-test_. The _t-test_ serves to show how different two samples are from each other and we will use it with dependent variables, as we want to measure the difference in personal parameters after an intervention (the introduction of a test with words that are incongruent with the colors). As we want to know if the samples are different from each other, the _t-test_ will be two-tailed, since the value of the _t-statistic_ can be very positive or very negative.

##### Report some descriptive statistics in relation to this data set. Include at least one measure of central tendency from at least one measure of variability.

As the tables below show, we have as a central tendency the mean, the median and the mode. As we have unique values, the data was gathered in a frequency table in which the data is inserted from its units.

|	Congruent	|	|	Incongruent	|
|	:------:	|	|	:------:	|
|	22.328	|	|	35.255	|
|	19.710	|	|	34.288	|
|	18.495	|	|	26.282	|
|	18.200	|	|	25.139	|
|	16.929	|	|	24.572	|
|	16.791	|	|	24.524	|
|	16.004	|	|	23.894	|
|	15.298	|	|	22.803	|
|	15.073	|	|	22.158	|
|	14.692	|	|	22.058	|
|	14.669	|	|	21.214	|
|	14.480	|	|	21.157	|
|	14.233	|	|	20.878	|
|	12.944	|	|	20.762	|
|	12.369	|	|	20.429	|
|	12.238	|	|	20.330	|
|	12.130	|	|	19.278	|
|	12.079	|	|	18.741	|
|	11.344	|	|	18.644	|
|	10.639	|	|	17.960	|
|	9.564	|	|	17.510	|
|	9.401	|	|	17.425	|
|	8.987	|	|	17.394	|
|	8.630	|	|	15.687	|

| | Congruent | Incongruent | 
|:-------|:------:|:------:|
|  Mean | 14.051  | 22.016 | 
|  Median | 14.357  | 21.018 | 
|  Mode | 12  | 17 and 20 | 
 
<br>
As measures of variability, we have the range, the interquartile range (IQR), and the standard deviation.

 
| | Congruent | Incongruent | 
|:-------|:------:|:------:|
| Range | 13.698  | 19.568 | 
| Q1 | 11.344  | 18.644 | 
| Q3 | 16.791  | 24.524 | 
| IQR | 5.447  | 5.880 | 
| SD | 3.559  | 4.797 | 

 
##### Provide one or two visualizations that show the distribution of the sample data. Write a sentence or two about what you observed from the chart or charts.

 ![Frequency](frequency.png "Frequency")

Analyzing the frequency charts, we can see that both have a tendency to normal distribution, but the sample size is small to show it clearly. Analyzing the ranges, we tend to think that the chart of the incongruous test is much more spread out, however, the values of the interquartile range are quite close, due to the fact that the incongruous test has outliers.


##### Now perform the statistical test and report your results. What is your level of confidence and critical statistical value? Did you reject the null hypothesis or failed to try to reject it? Find a conclusion regarding the task experiment. Are the results in line with your expectations?


For this _t-test_ we have two hypotheses:

H0: The two samples will have no substantial differences

H1: The two samples will be substantially different

The desired confidence interval is `99.5%`, that is, alpha level = `0.005`.

To find the value of the _t-statistic,_ we need the sample means, the standard deviation of the sample difference `S` and the sample size `n`. As we are dealing with samples, we have to infer the population standard deviation using Bessel's correction, so the variance will be divided by `23 (n-1)`. The sample means are shown in question’s 3 table.

|	Congruent	|	Incongruent	|	D	|	D-M	|	(D-M)^2	|
|	:------:	|	:------:	|	:------:	|	:------:	|	:------:	|
|	12.079	|	19.278	|	-7.199	|	0.766	|	0.586	|
|	16.791	|	18.741	|	-1.950	|	6.015	|	36.178	|
|	9.564	|	21.214	|	-11.650	|	-3.685	|	13.581	|
|	8.630	|	15.687	|	-7.057	|	0.908	|	0.824	|
|	14.669	|	22.803	|	-8.134	|	 -0.169	|	0.029	|
|	12.238	|	20.878	|	-8.640	|	 -0.675	|	0.456	|
|	14.692	|	24.572	|	-9.880	|	-1.915	|	3.668	|
|	8.987	|	17.394	|	-8.407	|	 -0.442	|	0.196	|
|	9.401	|	20.762	|	-11.361	|	-3.396	|	11.534	|
|	14.480	|	26.282	|	-11.802	|	-3.837	|	14.724	|
|	22.328	|	24.524	|	-2.196	|	5.769	|	33.279	|
|	15.298	|	18.644	|	-3.346	|	4.619	|	21.333	|
|	15.073	|	17.510	|	-2.437	|	5.528	|	30.556	|
|	16.929	|	20.330	|	-3.401	|	4.564	|	20.828	|
|	18.200	|	35.255	|	-17.055	|	-9.090	|	82.632	|
|	12.130	|	22.158	|	-10.028	|	-2.063	|	4.257	|
|	18.495	|	25.139	|	-6.644	|	1.321	|	1.744	|
|	10.639	|	20.429	|	-9.79	|	-1.825	|	3.331	|
|	11.344	|	17.425	|	-6.081	|	1.884	|	3.549	|
|	12.369	|	34.288	|	-21.919	| -13.954	|	194.720	|
|	12.944	|	23.894	|	-10.950	| -2.985	|	8.911	|
|	14.233	|	17.960	|	-3.727	|	4.238	|	17.959	|
|	19.710	|	22.058	|	-2.348	|	5.617	|	31.548	|
|	16.004	|	21.157	|	-5.153	|	2.812	|	7.906	|

| SS | Variance | S | t-statistic | 
|:-------|:------:|:------:|:------:|
| 544.330 | 23.667  | 4.865| -8.021| 


We have that the value of the _t-statistic_ is `-8.021`. As we chose the alpha level equal to `0.005` and the test is two-tailed, in Table T we look in column `0.0025` with 23 degrees of freedom, since the sample size is 24. The critical t value found is `3.091`.

 ![T Statistic](chart.png "T Statistic")

Since the value of the t-statistic found is within the critical region, below -t, we reject the null hypothesis, as we prove that the two samples are substantially different. The result was already expected, since the experiment was carried out by this author and the result showed a considerable difference between the times of the two tests (more than 7 seconds). At the beginning of the project we saw that the average of the incongruent test is very close to the last value of the congruent test (`22.328`), confirming the information that the times of the incongruent test are much longer than that of the congruent test.


##### Optional: What do you think is responsible for the observed effect? Can you think of an alternative or similar task that would result in a similar effect?

I imagine that as we pass our eyes over a word from the incongruent test, our subconscious automatically reads it and the delay in the response time would be caused by a conflict resulting from the our brain’s process of choosing between two words. When researching a little on the subject, I discovered that the name of this is semantic interference, because it only occurs when we use words. So I imagine two tests that would probably have the same result:

1 - A test with geometric shapes and, within them, the name of another geometric shape.
Example: A square with the word “triangle” inside it.

2 - A test showing images of actions, with a word describing another action below.

Example: An image of a person drinking water and below, the word “eating”


