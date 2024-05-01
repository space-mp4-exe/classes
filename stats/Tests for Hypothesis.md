# Basics
**Null Hypothesis** - $H_{0}$
- We reject a null hypothesis when sample statistics lie beyond a **critical value**
**Alternative Hypothesis** - $H_{1}$. The hypothesis that is true when the null hypothesis is false.
In a trial, the null hypothesis would be "not guilty" and the alternative would be "guilty".

**Error types**:
![[Tests for hypothesis-20240325105340104.webp]]Probability of a Type I error - $\alpha = P(H_{0} \;\text{is rejected} \mid H_{1} \;\text{is true})$
Probability of a Type II error - $\beta = P(H_{0} \; \text{is not rejected} \mid H_{1} \; \text{is false})$ 
# Rejection Regions
The rejection region is based on $\alpha$, our level of significance and the probability of Type I error. The rejection region is based on the probability that we reject $H_{0}$ when we shouldn't is $\alpha$. ![[Tests for Hypothesis-20240325110402199.webp]]

# Hypothesis Testing
There are two conditions, where $\sigma$ is known and where $\sigma$ is not known.
You should use the normal distribution if the population is normal and under 30 or if the population is over 30. 
If $\sigma$ is known, there are two methods:
- **Critical Value Approach** - determine some critical value and compare to $\alpha$.
- **$P$ Value Approach** - The probability of in the tail defined by the test statistic
---
**Critical Value Approach** 
Steps in the critical value approach  
- State the null and alternative hypotheses  
- Select the distribution to use  
- Determine the rejection and nonrejection regions and their associated critical values  
- Calculate the value of the test statistic  
- Compare the test statistic to the critical values  
- Make a decision
In these tests $z_{0}$ is called the *test statistic*.
$$
z_{0} = \frac{{\bar{y}-\mu_{0}}}{\sigma /\sqrt{ n }}
$$This equation is essentially a $Z$ score. This is the distance from $\mu$ in terms of standard deviations. 
Tires have some true average tread life $\mu$. A sample of 16 tires where drawn from a normal population with a $\sigma$ of 1500 miles. with 90% confidence ($\alpha$ is 0.1), we should learn when true average thread life is greater than 30000 miles. $\mu$ is 31000. 
$$
z_{0} = \frac{{\bar{y}-\mu_{0}}}{\sigma /\sqrt{ n }} = \frac{31000 - 30000}{1500 /\sqrt{ 16 }} = 2.76
$$
We want 90% confidence, which would be a $z$ value of 1.96, so we reject the null hypothesis that the true average thread life is less than 30000.

Ex. An engineer believes that the mean maximum snow load that will be applied on the roof of a building is less than 950 $N/m^2$. The maximum snow load was collected for each of the last 15 years, and the mean and standard deviation of this sample were 936 $\frac{N}{m^2}$ and 380 $\frac{N}{m^2}$. Use the critical value approach at 99% confidence.
$H_{0}:\mu\geq 950$. $H_{1}:\mu< 950$. $\bar{y}=935$, $s= 380$, $n=15$. $\alpha=0.01$. $t_{14,0.01}=-2.624$.
$$
t_{0}=\frac{\bar{y}-\mu_{0}}{s/\sqrt{ n }} = \frac{935-950}{380/\sqrt{ 15 }} =-0.153
$$
Do Not Reject Null Hypothesis.

$H_{0}: =$, $H_{1}: \neq$,$n=17$, $t_{0}=2.37$. we don't have a 2.37 value at a 16 degrees of freedom, so we say that the area on the tail is between 0.01 < area < 0.025. $\implies 0.02 < p-value<0.05$.

A food manufacturer claims that at the time of purchase by a consumer, the average age of its product is no more than 120 days.
$H_{0}: \mu\leq 120$, $H_{1}:\mu>120$, $\bar{y}=122.5$, $s=13.4$, $n=31$, $\alpha=0.05$. 
$t_{0}=\frac{122.5-120}{13.4/\sqrt{ 31 }} = 1.04$. We can tell from the t table that $t_{30,0.1}$ is more than $t_{0}$. This means that we do not reject the null hypothesis.  
The excel function is t.dist for left tail and t.dist.rt for right tail.

$H_{0}:\sigma^{2}\geq 7.5^{2}$. $H_{1}: \sigma^{2}<7.5^{2}$. $n$ = 30. $s$ = 6.35. 
$$
\begin{split}
\chi_{0}^{2} &= \frac{(n-1)s^{2}}{\sigma^{2}} \\
&= \frac{(30-1)6.35^{2}}{7.5^{2}} \\
\chi_{0}^{2} &= 20.788
\end{split}
$$ 