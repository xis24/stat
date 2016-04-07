**Time Series**
a sequence of observations in chronological order, for example, daily log returns on a stock or monthly values of the Consumer Price Index.

**Stochastic process**
a sequence of random variables and can be viewed as the theoretical or population analog of a time series. A time series can be considered a sample from the stochastic process.

**Stationary stochastic processes**
probability models for time series with time-invariant behavior.

**Strictly stationary**
all aspects of its behavior are unchanged by shifts in time; the probability distribution of a sequence of n observations does not depend on their time origin. 

**Weakly(covariance) stationary**
mean, variance and covariance are unchaged by time shifts. More precisely, Y1, Y2, ... is a weakly stationary process if 
* E(Yi) = u (a constat) for all i
* Var(Yi) = sigma^2 (a constant) for all i
* Corr(Yi, Yj) = rho (|i - j|) for all i and j for some function rho(h)
The adjective "weakly" in "weakly stationary" refers to the fact that we are only assuming that means, variance, and covariance, not other distributional characteristics such as quantitles, skewness, and kurtosis are stationary. 

The beauty of a stationary process is that it can be modeled with relatively few parameters.


**Two parameters that characterize a normal distribution**
1. The first parameter is SKEWNESS, which measures the symmetry in a distribution and is defined as the normalized third moment of a distribution. For distributions that are normally distributed, the skewness parameter is zero. Accordingly, we can test our returns data for normality by testing the null that are returns data have a skewness parameter of zero.
2. Another parameter used to define a normal distribution is KURTOSIS, or the normalized fourth moment, which characterizes the "peakedness" of a probability distribution. The normal distribution has kurtosis equal to 3, but fat-tailed distributions with extra probability mass in the tail areas have higher kurtosis. Accordingly, we can test our returns data for normality by testing the null that returns have a kurtosis parameter of 3, i.e., reject in favor of excess kurtosis.

**White noise**
Randomness. They are numbers that are independent but normally and identically distributed.

**Box-Jenkins**
Start with the series of interest(Y) and try to figure out what black box will take that series back to white noise. If you have the right black box, you will obtain white noise. If you have a wrong black box, you will not have white noise - which means you have not identified all the underlying parts of the series.

The black box is combination of moving average(MA) models and autoregressive(AR) models. ARMA: combining AR and MA into a single model.

**MA models**
Y is a function of past error terms, which themselves are nothing more than white noise. MA(q) model is:
    Y<sub>t</sub> = e<sub>t</sub> + W<sub>1</sub>e<sub>t-1</sub> + W<sub>2</sub>e<sub>t-2</sub> + ... + W<sub>q</sub>e<sub>t-q</sub>
    where e<sub>t</sub> is the white noise element from time t and W<sub>i</sub>is the weight of the corresponding white noise element.

**AR models**
a variable is a function of its previous values.
    Y<sub>t</sub> = A<sub>1</sub>Y<sub>t-1</sub> + A<sub>2</sub>Y<sub>t-2</sub> + ... + A<sub>p</sub>Y<sub>t-p</sub> + e<sub>t</sub>
    Where A's are coefficients, Y is the variable of interest and e<sub>t</sub> is a white noise error term. Here, since we have white noise, we can think there is link between MA and AR
The idea behind AR process is to feed past data back into the current value of the process. This induces correlation between the past and present. 

**ARMA models**
Put MA and AR together...
