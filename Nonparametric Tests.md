**Nonparametric** - not normally distributed
# Single Population - Sign Test
Rather than comparing how different a sample mean is from a hypothesized population mean, we count the deviations of each observation from the hypothesized **median**.
Value of interest $S$ = number of observation associated with positive/negative values of $y_{i} - \tau_{o}$.

For sample sizes of $n\geq 10$ 
$$
z_{0} = \frac{S-0.5n}{0.5\sqrt{ n }}
$$
Ex: We want to test the accuracy of the thermostat control at a 500$^{\circ}$F setting. We test 15 irons. 95% confidence. $H_{0}:\tau = 500$.
Values: We count how many differences are positive and how many are negative and pick the larger number of the the two. $S = max\{5,10\}$, so $S$ = 10.
494.6  - 500 = -, 510.8  - 500 = +, 487.5  - 500 = -, 493.2  - 500 = -, 502.6  - 500 = +, 485  - 500 = -, 495.9  - 500 = -, 498.2  - 500 = -, 501.6  - 500 = +, 497.3  - 500 = -, 492  - 500 = -, 504.3  - 500 = +, 499.2  - 500 = -, 493.5  - 500 = -, 505.8 - 500 = +
$$
z_{0} = \frac{10-0.5n}{0.5\sqrt{ n }} = \frac{10 - 0.5(7)}{0.5\sqrt{ 15 }} = 1.29
$$
$z_{0.05}$ = 1.645, We do not reject $H_0$. 
# Two Populations - Rank Sum Test
Let $D_{1}$ be the distribution of population 1 and $D_{2}$ be the distribution of population 2. We want to address
$H_{0}:$ Distributions $D_{1}$ and $D_{2}$ are the same. 
$H_{1}:$ Distributions $D_{1}$ lies to the (left, right, either) of $D_{2}$.
- left, lower-tailed test
- right, upper-tailed test
- either, two-tailed test
$$
z_{0} = \frac{T_{1}-\left[ \frac{n_{1}n_{2}(n_{1}+n_{2}+1)}{2} \right]}{\sqrt{ \frac{n_{1}n_{2}(n_{1}+n_{2}+1)}{12} }}
$$
