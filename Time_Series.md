**Time Series**
a sequence of observations in chronological order, for example, daily log returns on a stock or monthly values of the Consumer Price Index.

**Stochastic process**
a sequence of random variables and can be viewed as the theoretical or population analog of a time series. A time series can be considered a sample from the stochastic process.

**Stationary stochastic processes**
probability models for time series with time-invariant behavior.

**Strictly stationary**
all aspects of its behavior are unchanged by shifts in time; the probability distribution of a sequence of n observations does not depend on their time origin. 

**Weakly stationary**
mean, variance and covariance are unchaged by time shifts. More precisely, Y1, Y2, ... is a weakly stationary process if 
* E(Yi) = u (a constat) for all i
* Var(Yi) = sigma^2 (a constant) for all i
* Corr(Yi, Yj) = rho (|i - j|) for all i and j for some function rho(h)
The adjective "weakly" in "weakly stationary" refers to the fact that we are only assuming that means, variance, and covariance, not other distributional characteristics such as quantitles, skewness, and kurtosis are stationary. 

The beauty of a stationary process is that it can be modeled with relatively few parameters.