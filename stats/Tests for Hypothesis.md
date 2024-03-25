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

**Exam will go over slides 5, 6, 7**

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
z_{0} = \frac{{\bar{y}-\mu_{0}}}{\sigma /\sqrt{ n }} = \frac{31000 - 30000}{1500 /\sqrt{ 16 }}
$$
