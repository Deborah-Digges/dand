The Stroop Effect

1. What is our independent variable? What is our dependent variable?

Independent variable - type of words (congruent or incongruent) which is a Categorical variable
Depedent variable - time it takes to identify the color of the ink in which the word is printed which is a Quantitative variable

2. What is an appropriate set of hypotheses for this task? What kind of statistical test do you expect to perform? Justify your choices.

H0: Mean Time for identification(Congruent Word) - Mean Time for identification(Incongruent Word) = 0
H1: Mean Time for identification(Congruent Word) - Mean Time for identification(Incongruent Word) != 0

- In the null hypothesis, we assume that there is no relationship between the type of word(congruent vs incongruent) and the time it takes to identify the ink of the word
- In the alternate hypothesis, we assume that the type of word affects the time taken to identify the ink of the word, which results in the mean time taken for the two types of words being different

- Since the same person is measured twice, once for each of the conditions, this is a case of dependent samples and we would need to perform the *Paired T-test for Dependent Samples*
- As long as the sample is sufficiently large(> 30 by the central limit theorem), we should have no problem in performing this kind of test

3. Report some descriptive statistics regarding this dataset. Include at least one measure of central tendency and at least one measure of variability.

        Congruent   Incongruent
count   24.000000   24.000000
mean    14.051125   22.015917
std     3.559358    4.797057
min     8.630000    15.687000
25%     11.895250   18.716750
50%     14.356500   21.017500
75%     16.200750   24.051500
max     22.328000   35.255000

- The mean, standard deviation, min, 1st Quartile, Median, 3rd Quartile and the max for each category are show in the above table.
- The mean, median are measures of central tendency
- The standard deviation is a measure of variability

4. Provide one or two visualizations that show the distribution of the sample data. Write one or two sentences noting what you observe about the plot or plots.

- First we see the distribution of values of observation time for each category using side by side box plots. It can be seen that the time taken for observation in the congruent case is generally lower than the time for observation in the incongruent case. The first quartile of the incongruent category is greater than even the third quartile of the congruent category.

- Next we look at the shape of the distribution using Kernel Density Estimation. The distribution for the congruent category is centered at around 14 seconds and is unimodal with a normal distribution. The distribution for the incongruent case is shifted slightly to the right with a mean of around 22 seconds and is bimodal with a second peak at around 35 seconds.

5. Now, perform the statistical test and report your results. What is your confidence level and your critical statistic value? Do you reject the null hypothesis or fail to reject it? Come to a conclusion in terms of the experiment task. Did the results match up with your expectations?

test_statistic = x_d/(s_d / math.sqrt(n)) = -11.342992540180362
- x_d is the mean of the differences
- s_d is the standard deviation of the differences
- n is the number of subjects in the paired sample t test

confidence level = 95%

Since this is a two tailed test, we have the critical region defined by 2 critical values for df=n-1=23
Critical T value = [-2.011, 2.011]

The t-statistic lies well outside this range defined above and the probablity of having a t-statistic with this value is very close to 0.

Therefore we reject the null hypothesis and conclude that the type of word(congruent or incongruent) does indeed have an effect on the response time.

It does match up with my expectations as the time I took for the incongruent case was nearly double the time I took for the congruent case!

6. Optional: What do you think is responsible for the effects observed? Can you think of an alternative or similar task that would result in a similar effect? Some research about the problem will be helpful for thinking about these two questions!
- Reading more about the Stroop effect on Wikipedia, I see a number of reasons, but the most compelling one seems to be the fact that the brain processes written information much more "automatically" than it perceives information about color. Hence, if the word "red" is written in the color green, the textual information "red" reaches the brain before the perceptual information reaches the brain, causing interference between the two reactions.
- An alternate task that produces the same effect is the Numerical Stroop Effect in which congruent numbers are ones in which the digit size is proportional to the numerical value(For example a big digit 5 and a small digit 3). Incongruent numbers are those in which the digit size is inversely proportional to the numerical value (For example, a big digit 3 and a small digit 5). Identifying the digit in the incongruent case would take more time than in the congruent case

