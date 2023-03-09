## Probability & Random Variables

Probability = no. of possible outcomes / total no. of outcomes

Eg: Rolling a dice
Sample space : set of numbers from 1 to 6
Probability of random variable, P(X=2) = 1/6    here, 2 is a random variable -> it is discrete

Discrete: countable sample space  -> eg: rolling a dice
Continuous: sample space is a range of real numbers, or a whole set of real numbers   -> time when the bus arrives

## Probability Distribution

difficult to describe the probability distribution of a continuous variable

probability density function p(x)

![image](https://user-images.githubusercontent.com/15999442/220876558-8084e1d9-8366-4992-b05d-a0cde286b3f6.png)

## Mean, Variance and Standard Deviation

#### Mean

Mean is the average value of all the numbers

mean (arithmetic avg) = (x1, x2, ... xn)/n

when sample increases, i.e., n→∞,

mean (expectation), ![image](https://user-images.githubusercontent.com/15999442/220879352-a98b3b36-277f-403d-a996-25bbd2efaa6f.png)             (values {x1, x2, ..., xN} and corresponding probabilities p1, p2, ..., pN)

#### Variance 

Standard Deviation is a measure of how spread out the numbers are from the mean

variance, ![image](https://user-images.githubusercontent.com/15999442/220879412-29ac57f6-b2f2-4f17-b3b0-296a4fe62f1b.png)         (μ = mean of the sequence)

σ   -> standard deviation
σ^2 -> variance

A low variance indicates that the values in the dataset are close to the mean, while a high variance indicates that the values are spread out over a wider range.
2 datasets with different values can have the same variance if the differences between the values and their respective means are similar in both datasets.
`
Dataset 1: [1, 2, 3, 4, 5]
Dataset 2: [100, 101, 102, 103, 104]
`
Here, both have same variance

Whether a calculated variance is considered high or low depends on the context of the data being analyzed.
One way to determine if a variance is high or low is to compare it to the mean of the dataset. If the variance is relatively small compared to the mean, then the data can be said to have low variability. Conversely, if the variance is relatively large compared to the mean, then the data can be said to have high variability.
Another approach is to compare the variance to other datasets that are similar in nature or context.

## Mode, Median and Quartiles

when there are a few extreme values that are completely out of range, they can affect the mean

Median -> a value such that half of data points are lower than it, and another half - higher

Quartiles
- First quartile, Q1, is a value, such that 25% of the data fall below it
- Third quartile, Q3, is a value that 75% of the data fall below it

Mode -> good "typical" value -> value that appears the most frequently

###  Mean, Median, Mode, and Variance in Data Science

- Mean: 
The mean is used to measure the central tendency of a dataset, and is often used when the data is normally distributed and has no significant outliers. It is the most commonly used measure of central tendency in data science, and is often used in hypothesis testing and predictive modeling.

- Median:
The median is also used to measure the central tendency of a dataset, but is more robust to outliers than the mean. It is often used when the data is skewed or has significant outliers, as it provides a better estimate of the "typical" value. The median is often used in descriptive statistics and exploratory data analysis.

- Mode: 
The mode is used to measure the most common value or values in a dataset. It is often used when the data is categorical or discrete, and provides insight into the distribution of the data. The mode is often used in market research and survey analysis.

- Variance: 
The variance is used to measure the spread of a dataset, and is often used in combination with the mean. It provides insight into how much the data varies from the mean, and is often used in hypothesis testing and predictive modeling. The variance is also used to calculate other statistical measures, such as the standard deviation and coefficient of variation.

## Normal Distribution

Normal distribution is a way to describe how numbers tend to be spread out. It's like looking at the heights of all the students in your class - some are really tall, some are really short, and most are somewhere in the middle. If you made a graph of all the heights, it would probably look like a hill with most of the students in the middle and fewer at the extremes.

In machine learning and data science, normal distribution is a way to describe the pattern of numbers in a dataset. It's also called the "bell curve" because when you graph the numbers, it looks like a bell.

The normal distribution tells us how many of the numbers in the dataset are close to the average, and how many are far away. For example, if you looked at the grades of all the students in your class, you might see that most students got grades around a C, and fewer students got grades that were very high or very low.

Normal distribution is really important in data science because it helps us understand how likely it is that a particular number or event will happen. It also helps us make predictions based on past data. So, if we know that a certain dataset follows a normal distribution, we can use that information to make better decisions and predictions in the future.

### How to calculate Normal Distribution

To calculate normal distribution, you need to know two things: the mean and the standard deviation of the dataset.

Once you have the mean and standard deviation, you can use a formula called the normal distribution equation to calculate the probability of a particular value occurring in the dataset.
normal distribution equation:

P(x) = (1 / (σ * sqrt(2π))) * e^(-(x-μ)^2 / (2σ^2))

Here, P(x) is the probability of a particular value x occurring in the dataset, μ is the mean, σ is the standard deviation, e is the mathematical constant approximately equal to 2.71828, and π is the mathematical constant approximately equal to 3.14159.

To use the equation, you need to substitute the values of μ, σ, and x into the equation and solve for P(x). The result will give you the probability of x occurring in the dataset.

There are also many software tools, such as Excel or Python, that can perform normal distribution calculations for you. These tools make it easier to calculate probabilities for large datasets or complex situations.

If you want to train a machine learning model on a dataset, you can use the `np.random.normal()` function to generate a random dataset that follows a normal distribution with a specific mean and standard deviation. This can help you test and optimize your model before applying it to real-world data.

### Different methods to determine if the distribution is Normal or not

- **Histogram and Density Plots:** This method is commonly used as a visual aid to get a sense of the shape of the data distribution. It is useful for small and large datasets, but it can be subjective and may not always accurately indicate whether the distribution is normal or not.

- **Q-Q Plot:** This method is useful for comparing the distribution of the data to the theoretical normal distribution. It is commonly used for small and large datasets, but it can be difficult to interpret for non-experts.

- **Shapiro-Wilk Test:** This is a commonly used statistical test for small to medium-sized datasets (up to a few thousand observations) and is considered to be more powerful than the Anderson-Darling test. It provides a p-value that indicates the probability of the data coming from a normal distribution.

- **Anderson-Darling Test:** This is a commonly used statistical test for small to medium-sized datasets (up to a few thousand observations) and is considered to be more sensitive than the Shapiro-Wilk test. It provides a p-value that indicates the probability of the data coming from a normal distribution.

It is a good practice to use multiple methods to check for normality, and to consider the results in combination with other factors, such as the skewness and kurtosis of the data distribution, the sample size, and the specific requirements of the analysis.

### Confidence Intervals

Confidence intervals are a way to measure how certain we are about our estimates.

Imagine you are trying to guess the weight of a big pumpkin, but you can't pick it up. Instead, you can only estimate its weight by looking at other pumpkins of similar size. However, you know that your estimate might not be exactly right because each pumpkin is a little different. So, to help you get a better idea of the pumpkin's weight, you can use confidence intervals.

A confidence interval is like a range of possible weights that the pumpkin could be, based on the pumpkins you have seen before. For example, if you estimate that the pumpkin weighs 50 pounds and you have a 95% confidence interval, that means you are 95% sure that the pumpkin's true weight is somewhere between 45 and 55 pounds.

In data science, we use confidence intervals to estimate things like the average height of people, the mean income of a city, or the accuracy of a machine learning model. By using confidence intervals, we can get a better idea of how accurate our estimates are and how much uncertainty there is in our data.

Overall, confidence intervals help us to make better predictions and decisions by giving us a sense of how certain we can be about our estimates.

#### Higher the confidence probability, Wider the confidence interval

When we construct a confidence interval, we are trying to estimate the true value of a population parameter (such as the population mean or population proportion) based on a sample of data. The confidence interval represents a range of values within which we believe the true population parameter lies with a certain level of confidence.

The level of confidence is typically expressed as a percentage, such as 95% or 99%. This percentage represents the proportion of all possible samples that would produce an interval containing the true population parameter. For example, a 95% confidence interval means that if we were to repeat the same study many times and calculate a confidence interval each time, we would expect that 95% of those intervals would contain the true population parameter.

The width of the confidence interval is affected by several factors, including the sample size, the standard deviation of the sample, and the level of confidence. A higher level of confidence requires a wider interval because we want to be more certain that the true population parameter falls within the interval. Similarly, a larger standard deviation or a smaller sample size will result in a wider interval because there is more uncertainty in our estimate of the population parameter.

So, in summary, a higher level of confidence requires a wider interval because we want to be more confident that the true population parameter falls within the interval, and this wider interval allows for more uncertainty in our estimate.

Typically we calculate the confidence interval for a sample data, not for the entire population. The reason for this is that it is not possible to calculate the confidence interval for a population since we usually do not have access to the entire population data.
Instead, we take a random sample from the population and use that to estimate the parameters of the population, such as the population mean. We can then use the sample mean and sample standard deviation to calculate the confidence interval for the population mean. The confidence interval provides a range of values that is likely to contain the true population mean with a certain level of confidence.

## Hypothesis Testing

Hypothesis testing is a way to find out if something is true or not.

For example, let's say you have a friend who claims they can predict the weather by looking at the clouds. You might be skeptical and want to test their claim.
So, you come up with a hypothesis, which is basically a guess or prediction about what you think will happen. Your hypothesis might be something like, "My friend can't predict the weather by looking at the clouds."
Next, you collect some data by observing your friend's cloud predictions and comparing them to the actual weather.
Then, you use statistics to analyze the data and see if it supports or contradicts your hypothesis.
If the data supports your hypothesis, you might conclude that your friend's claim is not true. But if the data contradicts your hypothesis, you might have to accept that your friend's claim might be true after all.

Overall, hypothesis testing is a way to help us make decisions and draw conclusions based on evidence and data.

### Student t-test
If we know that our distributions are normal, we can apply Student t-test.
> t-test is a statistical test used to compare two groups of data and determine whether the difference between their means (averages) is statistically significant or just due to chance.

#### t-value 

> The t-value is a measure of the difference between the means of two groups of data, scaled by the variation within each group. It tells us how large the difference between the two groups is relative to the variation within each group.

python library used: **ttest_ind**
- equal_var - equal or unequal variances

#### p-value

The p-value, or probability value, is a measure of the probability that the observed difference between the two groups of data is due to chance alone. It is used to determine if the difference between the two groups is statistically significant, which means that it is unlikely to be due to chance.

### Law of Large Numbers and Central Limit Theorem

#### Law of Large Numbers

The Law of Large Numbers is a fundamental concept in probability theory that states that as the number of independent trials of an experiment increases, the average value of the outcomes will converge towards the expected value of the experiment. In simpler terms, this means that if we repeat an experiment many times, the average of the results will be close to the expected value of the experiment.

Eg: if we toss a fair coin many times, the Law of Large Numbers tells us that the proportion of heads will converge towards 0.5 as the number of coin tosses increases. This concept is important in data science and machine learning because it allows us to make accurate predictions about future outcomes based on a large sample of data.

#### Central Limit Theorem

The Central Limit Theorem is another important concept in statistics that states that as the sample size of a random variable increases, the distribution of sample means approaches a normal distribution, regardless of the underlying distribution of the variable itself. In simpler terms, this means that if we take many random samples of the same size from a population, the distribution of the sample means will be approximately normal.

Eg: if we take many random samples of size 30 from a population with an unknown distribution, the Central Limit Theorem tells us that the distribution of the sample means will be approximately normal, regardless of the underlying distribution of the population. This concept is important in statistical inference because it allows us to use the normal distribution to make inferences about population parameters, even when the population distribution is unknown.


### Covariance and Correlation

> ONLY WORKS ON NUMERICAL VALUES

We say that two sequences correlate when they exhibit the similar behavior at the same time, i.e. they either rise/fall simultaneously, or one sequence rises when another one falls and vice versa. In other words, there seems to be some relation between two sequences.

Correlation does not necessarily indicate causal relationship between two sequences; sometimes both variables can depend on some external cause, or it can be purely by chance the two sequences correlate. However, strong mathematical correlation is a good indication that two variables are somehow connected.

Mathematically, the main concept that shows the relation between two random variables is covariance, that is computed like this: **Cov(X,Y) = E[(X-E(X))(Y-E(Y))]**. 
We compute the deviation of both variables from their mean values, and then product of those deviations. 
- If both variables deviate together, the product would always be a positive value, that would add up to positive covariance. 
- If both variables deviate out-of-sync (i.e. one falls below average when another one rises above average), we will always get negative numbers, that will add up to negative covariance. 
- If the deviations are not dependent, they will add up to roughly zero.

The absolute value of covariance does not tell us much on how large the correlation is, because it depends on the magnitude of actual values. To normalize it, we can divide covariance by standard deviation of both variables, to get correlation. 

Correlation is always in the range of [-1,1]
- 1 : indicates strong positive correlation between values
- -1 : strong negative correlation
- 0 : no correlation at all (variables are independent)

> print(np.corrcoef(column1,column2))

