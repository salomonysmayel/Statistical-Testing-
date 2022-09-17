# Statistical-Testing

# Project Report 
# By Carlos Ysmayel                                          IEOR E4150 Professor. Dr. A. B Dieker  
# Columbia University. Department of Engineering 

## Analysis on Tesla, Inc.

## Data Set Description

The data used on this project consist of 9 daily historical stocks prices of companies that belong to either the automotive or the technology sector and one stock market index, the Nasdaq Composite. The data ranges from November 27th, 2018 to November 25th 2020, encompassing 504 data points of open and closing prices. These securities are

## Automotive sector 

Tesla, Inc. (TSLA)
Daimler AG (DAI.DE)
Toyota Motor Corporation (TM)
General Motors Company (GM)
Ford Motor Company (F)

## Technology sector

Apple Inc. (AAPL)
Alphabet Inc. (GOOG)
Dell Technologies Inc. (DELL)
Microsoft Corporation (MSFT)

## Index

NASDAQ Composite (^IXIC)

## Objectives

Since its inception the automotive industry comprises almost entirely the same big old companies, namely, Ford, General Motors, Toyota, Daimler, among a few others. It seems the word “newcomer” is anathema to this industry. If a company manages to get started, it takes many decades to become as big as the competition. Four out of the five automakers listed here were founded at least 84 years ago. One may speculate that this is due to the enormous amount of knowledge and resources needed from the very beginning, most likely with no propecs of profits on the near horizon , and then, the difficulties of gaining customers that would rather buy a car from a long trusted manufacturer. However, Tesla, Inc. has proven by its meteoric rise to be an exception to the rule. Founded in 2003, it has had a growth that appears to be antithetic to the movements and developments of the automobile industry, with a current market capitalization of 578,21 B, the biggest for an automaker, been trailed in second place by Toyota with a market capitalization of 211,66 B. It seems that Tesla's growth mimics more the behaviour of a tech company, like Google or Apple, which in just a few years since its foundations were taking over the world. It may be interesting to explore this idea statistically, and to give advice to our clients on how to llok at Tesla, if we should be addressed as a successful car manufacturer. In order to achieve this the following analysis structure based on the log-returns of the securities was followed.


An individual study to elucidate the behavior of each security’s returns.  This allows us to see how Tesla compares with the other companies in terms of profitability and volatility over the period of time considered. In addition a linear regression on time supports the observations. 

A pairing based  statistical analysis of the returns of Tesla with the other companies, by computing correlations,  testing the equality of the two average returns considering both the case of unknown and unequal variances and a paired test. This was followed by linear regressions of Tesla against the others. Additionally all the companies were analyzed against the Nasdaq composite to have background on how the securities behave in comparison with the tech market since Nasdaq is mostly constituted by technology companies.  

Finally a multiple linear regression was performed of Tesla against all the automotive companies and Tesla against all the tech companies to compare Tesla against both industries.  

## Analysis

The histogram of the log-return shows that the distribution of these values for all the securities is approximately normal. Also, the data was plotted against the theoretical normal distribution, corroborating that in all cases the log-returns form an approximate line, indicating that there is approximate normality in the data points with R^2 coefficients all over 0.85.

To visualize the returns as a time series we plotted together all the securities. They all overlap forming a very noisy looking plot, however we can tell that a few companies diverge more than others from the cluster, as we can see in the next graphic.

![model setup](/IMAGES/returns.png)

Just by looking at this graph we should expect a higher volatility from Tesla, that shows in green deviating more than the other time series curves that appear clustered around zero even at 2020-04 at the first peak of the global pandemic that shows an increase in variance for all the securities. 

Considering  95% confidence, we proceed to perform parameter estimation on the mean and variance of the returns. Since we cannot assume equality in the population variances for the means we need to construct a t-random variable with n-1 degrees of freedom to obtain the confidence interval. Likewise, for the variance a statistic with chi squared n-1 degrees of freedom distribution was computed to obtain the interval. 

![model setup](/IMAGES/confidence_intervals_mean_variance.png)

These results show that the average returns are very close to zero for all the securities, however, all the intervals have more mass on one side than the other, indicating that the returns are almost zero but in all cases with more mass on the positive side of the interval. Also we can see that the variance is very small, but comparing the values we see that the companies in the stock sector have a broader interval, and the automotive sector with the most restricted variances, except for tesla. This may indicate that the tech sector is more volatile than the automotive sector, and that Tesla inclines more to the first and less to the latter. 


![model setup](/IMAGES/linear_reg_returns.png)

Went plotting the lines that resulted from the linear regression over time we can see that since the slope is close to zero, just as the data points over time don't diverge too much from zero as we saw on the first study. However our coefficient of determination in all cases is so low that we see the amount of variation on the returns cannot be explained by time.

## Pairing based  Analyses

First we perform a hypothesis testing for the equality of the means, first by a case of unknown and unequal variances and second by a paired t-test. If there is no underlying trend affecting both variables at the same time then the result of both tests should be approximate. On both we have a comparison of tesla against all the other companies, on the t-test we also have the results of all the companies against the Nasdaq, that we are considering here to be approximate in behavior to the market. 

![model setup](/IMAGES/tests_means.png)

On the first test for equality of means on all the comparisons we are not able to reject the hypothesis that the means are equal. However we find that for higher p-values, closer statistic value to zero, hence for a given alpha, an interval where the means tend more to be equal. Following this logic we find that tesla compared to the tech companies, like google (p-value 0.95), even Dell, (0.45) the lowest p-value for Tesla with a tech company on this test, these values are all higher that tesla compared to any car manufacturer except for Daimler (0.49).

On the paired test we get different results, the p-values are lower, however, we manage to reject just two null hypothesis, that Ford mean is equal to Nasdaq, and that Toyota mean is equal to Nasdaq, this should not come as a surprise because Toyota not only is not a tech company, but is not even an American company. However we find similar comparison results as to the previous equality of means test. Were the highest p-values come from tesla-apple and tesla-google, two of the biggest tech companies in the world. 

We also have a Linear Regression analysis of Tesla against the other companies, these are the results,

![model setup](/IMAGES/linear_reg_tesla_vs_all.png)

We see from the coefficients of determination that the amount of variation in the response variable is better explained by the input variables in the case of the tech companies. 

Finally we performed a couple of  Multiple Linear Regressions, one Tesla against all the tech companies and one of Tesla against all the automakers. The coefficient of determinations obtained are, Tesla against Tech 0.15, and tesla against all automakers 0.11. Where we see that Tesla’s returns variations are better explained by the tech sector. 

## Conclusions 

Knowing that it is very difficult to understand the causes of the behavior of securities, in this study we can at least tell the clients that Tesla is not your typical Automaker, for better or worse. Its behavior is not comparable to its own industry, it may have more commonalities with others, such as the tech industry. This opens the possibilities of even more questions. Is Tesla actually a car manufacturer or should be considered more a technology company offering cars at the moment, or is it because it is changing its own industry, or is even too risky of a company to invest in, maybe driven by hype and pop culture. Difficult to tell. But what we can do is statistically say, given the results of this test, that Tesla’s historic returns are not those of your usual successful car manufacturer. There is much more here happening and we need to continue studying this case.




