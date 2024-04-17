# Estimation
we use $\bar{y}$ to represent the mean of a sample population. This is different from $\mu$ because $\mu$ is the mean of the entire population. $\bar{y}$ only represents the mean of one particular sample taken. 
In the same way, we use $\hat{p}$ to denote the portion population. These are called *estimators*.
***
## Point and Interval Confidence
The sample means, $\bar{y}$, is only one point, called a point estimate. The problem with this is that it might not be representative of the whole population, so we use intervals of confidence to counter this.
With intervals of confidence we can say that "our sample mean is 14, and maybe our population mean, $\mu$, is the same." "We are $x\%$ confident that the true mean lies between points $a$ and $b$."

We can find an interval of confidence from the standard deviation of a sample. 
$\sigma_{\bar{y}} = \sigma/\sqrt{ n }$ 
This equation gives us standard deviation based on sample size. 
Confidence level is denoted as $(1-\alpha)100\%$. $\alpha$ is the significance level. This equation gives the confidence interval for $\mu$.
$$
\mu= \bar{y} \pm Z_{\frac{\alpha}{2}} \frac{\sigma}{\sqrt{ n }}
$$

![[Statistical Intervals for a Single Population-20240325170357995.webp]] We can see from the graph that $\alpha$ is a portion of the curve around the mean. 

To find the interval of confidence when you don't know $\sigma$, you should use a $t$ distribution. This distribution is based on something called *degrees of freedom*. $df = n-1$. The equation to find the interval of confidence is 
$$
\bar{y} \pm t_{df, \alpha / 2} \frac{s}{\sqrt{ n }}
$$
To find $t_{df, \alpha / 2}$, you simply just have to look it up in a $t$ table.
***
## Examples
Say that we’re interested the ability of a particular kind of lumber to withstand loading 
- Assume we know that the population of eastern white pine lumber has a modulus of elasticity standard deviation of $\sigma$ = 1,550 MPa
-  Based on our sample of $n$ = 40, $\bar{y}$ is 13,985 MPa  
- Assume 95% confidence
Find $\mu$ from this.

Our $\alpha$ is 0.05 because 0.95 = (1-0.05), refer to the bell curve image above. Now we have to find $Z_{\frac{\alpha}{2}}$, it is equal to the far ends of the tails of the bell curve. We can do this by finding the $Z$ score of the area in between the tail ends. Half of (1 - 0.05) is 0.475, the $Z$ score needed for this probability is 1.96, this is what $Z_{\frac{\alpha}{2}}$ is. ![[Statistical Intervals for a Single Population-20240325173548856.webp|481]]
We put these all together to get 
$$
\begin{split}
\mu= \bar{y} \pm Z_{\frac{\alpha}{2}} \frac{\sigma}{\sqrt{ n }} \\
= 13985 \pm 1.96 \frac{1550}{\sqrt{ 40 }} \\
\mu = [13504.65, 14465.35] \; \text{MPa}
\end{split}
$$

Now remember this means that we are 95% confident that $\mu$ lies somewhere within this interval.

Say we want to estimate the mean repair time of a brand new circuit board design. 
$n$ = 23, $\bar{y}$ = 14.9, $s$ = 5.4, assume 95% confidence (so $\alpha$ is 0.05). All of these variables means that $t_{df, \alpha / 2}$ is $t_{22,0.025}$. From the lookup table, we that $t_{22,0.025}$ = 2.074. Putting all of these together, we get $$
\begin{split}
\mu = \bar{y} \pm t_{df, \alpha / 2} \frac{s}{\sqrt{ n }} \\
14.9 \pm 2.074 \frac{5.4}{\sqrt{ 23 }} \\
\mu = [12.56, 17.24]
\end{split}
$$
# Confidence interval for variance
$$
\frac{(n-1)s^2}{\sigma^2} \sim \chi^2
$$
$$
\begin{split}
\chi^{2}_{1-\frac{\alpha}{2}} \leq \frac{(n-1)^{2}}{\sigma^{2}} \leq \chi^{2}_{\frac{\alpha}{2}} \\
\frac{1}{\chi^{2}_{\frac{\alpha}{2}}} \leq \frac{\sigma^{2}}{(n-1)^{2}s^{2}}\leq \frac{1}{\chi^{2}_{1-\frac{\alpha}{2}}} \\
\frac{(n-1)^{2}s^{2}}{\chi^{2}_{\frac{\alpha}{2}}}\leq \sigma^{2} \leq \frac{(n-1)^{2}s^{2}}{\chi^{2}_{1- \frac{\alpha}{2}}}
\end{split}
$$
Consider the task completion time data set
what is the 90% confidence interval for variance?
$S$=4.358. $n$ = 30. $\alpha$ = 0.1. $\chi^{2}_{29.95} = 17.7083$. $\chi^{2}_{29.05} = 42.5569$
$$
\begin{split}
\frac{(30-1)4.358^{2}}{42.5569}\leq\sigma^{2}\leq \frac{(30-1)4.358^{2}}{17.7078} \\
\sigma^{2}:[12.94, 31.1]\sec^{2} \\
\sigma:[3.597, 5.577]\sec
\end{split}
$$
We can say that that we are 90% sure that $\mu$ for time completion is between 3.597 and 5.577 seconds.
$$
\mu: \bar{y} \pm t_{(df_{1} \frac{\alpha}{2})} \frac{s}{\sqrt{ n }}
$$
$$
p: \hat{y} 
$$
There are 400 customer orders from ElectriCity
 - what is a 99% confidence interval for the mean?
 - the 99% CI for the standard deviation of the total cost of orders? 
 
From data set: $\bar{y}$: 153.82, $s$: 97.37, $n$: 400, $\alpha$: .01 $t_{399.005}$:2.588 $\leftarrow$ (from excel's t.inv.2t function)
$$
\begin{split}
\bar{y} \pm t_{399.005} \frac{s}{\sqrt{ n }} \\
153.82 \pm 2.588 \frac{97.37}{\sqrt{ 400 }} \\
[141.22, 166.42]
\end{split}
$$
$s$ = 97.37, $n$= 400, $\alpha$ = 0.01, $\chi^{2}_{399.005}$= 475.513, $\chi^{2}_{399.995}$ = 329.9939.
$$
\begin{split}
\frac{(400-1)97.37^{2}}{475.5153}\leq \sigma^{2} \leq \frac{(400-1)97.37^{2}}{329.9939} \\
\sigma^{2}= [7955,11464]^{2} \\
\sigma = [89.19,107.07]
\end{split}
$$
