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

mean (arithmetic avg) = (x1, x2, ... xn)/n

when sample increases, i.e., n→∞,

mean (expectation), ![image](https://user-images.githubusercontent.com/15999442/220879352-a98b3b36-277f-403d-a996-25bbd2efaa6f.png)             (values {x1, x2, ..., xN} and corresponding probabilities p1, p2, ..., pN)

#### Variance 
how far the values are spread

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
- The mean is used to measure the central tendency of a dataset, and is often used when the data is normally distributed and has no significant outliers. It is the most commonly used measure of central tendency in data science, and is often used in hypothesis testing and predictive modeling.

- Median:
- The median is also used to measure the central tendency of a dataset, but is more robust to outliers than the mean. It is often used when the data is skewed or has significant outliers, as it provides a better estimate of the "typical" value. The median is often used in descriptive statistics and exploratory data analysis.

- Mode: 
- The mode is used to measure the most common value or values in a dataset. It is often used when the data is categorical or discrete, and provides insight into the distribution of the data. The mode is often used in market research and survey analysis.

- Variance: 
- The variance is used to measure the spread of a dataset, and is often used in combination with the mean. It provides insight into how much the data varies from the mean, and is often used in hypothesis testing and predictive modeling. The variance is also used to calculate other statistical measures, such as the standard deviation and coefficient of variation.
