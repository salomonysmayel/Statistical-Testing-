# Statistical-Testing

Project Report 
By Carlos Ysmayel                                          IEOR E4150 Professor. Dr. A. B Dieker              

Analysis on Tesla, Inc.

Data Set Description

The data used on this project consist of 9 daily historical stocks prices of companies that belong to either the automotive or the technology sector and one stock market index, the Nasdaq Composite. The data ranges from November 27th, 2018 to November 25th 2020, encompassing 504 data points of open and closing prices. These securities are

Automotive sector 

Tesla, Inc. (TSLA)
Daimler AG (DAI.DE)
Toyota Motor Corporation (TM)
General Motors Company (GM)
Ford Motor Company (F)

Technology sector

Apple Inc. (AAPL)
Alphabet Inc. (GOOG)
Dell Technologies Inc. (DELL)
Microsoft Corporation (MSFT)

Index

NASDAQ Composite (^IXIC)

Objectives

	Since its inception the automotive industry comprises almost entirely the same big old companies, namely, Ford, General Motors, Toyota, Daimler, among a few others. It seems the word “newcomer” is anathema to this industry. If a company manages to get started, it takes many decades to become as big as the competition. Four out of the five automakers listed here were founded at least 84 years ago. One may speculate that this is due to the enormous amount of knowledge and resources needed from the very beginning, most likely with no propecs of profits on the near horizon , and then, the difficulties of gaining customers that would rather buy a car from a long trusted manufacturer. However, Tesla, Inc. has proven by its meteoric rise to be an exception to the rule. Founded in 2003, it has had a growth that appears to be antithetic to the movements and developments of the automobile industry, with a current market capitalization of 578,21 B, the biggest for an automaker, been trailed in second place by Toyota with a market capitalization of 211,66 B. It seems that Tesla's growth mimics more the behaviour of a tech company, like Google or Apple, which in just a few years since its foundations were taking over the world. It may be interesting to explore this idea statistically, and to give advice to our clients on how to llok at Tesla, if we should be addressed as a successful car manufacturer. In order to achieve this the following analysis structure based on the log-returns of the securities was followed.


An individual study to elucidate the behavior of each security’s returns.  This allows us to see how Tesla compares with the other companies in terms of profitability and volatility over the period of time considered. In addition a linear regression on time supports the observations. 

A pairing based  statistical analysis of the returns of Tesla with the other companies, by computing correlations,  testing the equality of the two average returns considering both the case of unknown and unequal variances and a paired test. This was followed by linear regressions of Tesla against the others. Additionally all the companies were analyzed against the Nasdaq composite to have background on how the securities behave in comparison with the tech market since Nasdaq is mostly constituted by technology companies.  

Finally a multiple linear regression was performed of Tesla against all the automotive companies and Tesla against all the tech companies to compare Tesla against both industries.  

Analysis

The histogram of the log-return shows that the distribution of these values for all the securities is approximately normal. Also, the data was plotted against the theoretical normal distribution, corroborating that in all cases the log-returns form an approximate line, indicating that there is approximate normality in the data points with R^2 coefficients all over 0.85.

To visualize the returns as a time series we plotted together all the securities. They all overlap forming a very noisy looking plot, however we can tell that a few companies diverge more than others from the cluster, as we can see in the next graphic.



