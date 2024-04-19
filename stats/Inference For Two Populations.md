We have two versions of each of the stats for each population. $\bar{y}_{1}$ = sample mean of population 1. $\bar{y}_{2}$ = sample mean of population 2. $\sigma_{1}$ = std div of pop 1. $\sigma_{2}$ = std div of pop 2. 

$$
\begin{split}
\mu_{\bar{y_{1}}-\bar{y}_{2}} = \mu_{1} - \mu_{2} \\
\sigma_{\bar{y_{1}}-\bar{y}_{2}} = \sqrt{ \frac{\sigma^{2}_{1}}{n_{1}} - \frac{\sigma^{2}_{2}}{n_{2}}} \\
(1-\alpha)100\% = \mu_{\bar{y_{1}}-\bar{y}_{2}}\pm z_{\alpha / 2}\sigma_{\bar{y_{1}}-\bar{y}_{2}}\\
= (\bar{y}_{1}-\bar{y_{2}})\pm z_{\alpha / 2}\sqrt{ \frac{\sigma^{2}_{1}}{n_{1}} - \frac{\sigma^{2}_{2}}{n_{2}}}
\end{split}
$$
# Difference in $\mu$
with $\sigma$ unknown. 

$\sigma$ is assumed to be **equal** for these equations 
Confidence formula
$$
\begin{split}
s_{p} = \sqrt{ \frac{(n_{1}-1)s^{2}_{1}+(n_{2}-1)s^{2}_{2}}{n_{1}+n_{2}-2} } \\
(1-\alpha)100\% = \bar{y}_{1-2}\pm t_{df,\alpha / 2}s_{1-2} \\
=(\bar{y}_{1}-\bar{y_{2}})\pm t_{df, \alpha / 2}\sqrt{ \frac{(n_{1}-1)s^{2}_{1}+(n_{2}-1)s^{2}_{2}}{n_{1}+n_{2}-2}}\sqrt{ \frac{1}{n_{1}}+\frac{1}{n_{2}} }
\end{split}
$$
$t_{0}$ test formula
$$
\begin{split}
t_{0} =\frac{(\bar{y}_{1}-\bar{y}_{2})-(\mu_{1}-\mu_{2})}{s_{\bar{y}_{1}-\bar{y}_{2}}} \\
t_{0} = \frac{(\bar{y}_{1}-\bar{y}_{2})-(\mu_{1}-\mu_{2})}{\sqrt{ \frac{(n_{1}-1)s^{2}_{1}+(n_{2}-1)s^{2}_{2}}{n_{1}+n_{2}-2}}\sqrt{ \frac{1}{n_{1}}+\frac{1}{n_{2}} }}
\end{split}
$$
$df$ is calculated as 
$$
df = df_{1} - df_{2} = (n_{1}-1)+(n_{2}-2)=n_{1}+n_{2}-2
$$

Ex: $n_{1}$ = 35, $\bar{y}_{1}$ = 4.1, $s_{1}$ = 1.8, $n_{2}$ = 27, $\bar{y}_{2}$ = 4.5, $s_{2}$ = 2.0 $H_{0}:\mu_{1} = \mu_{2}$
$$
\begin{split}
t_{0} = \frac{(\bar{y}_{1}-\bar{y}_{2})-(\mu_{1}-\mu_{2})}{\sqrt{ \frac{(n_{1}-1)s^{2}_{1}+(n_{2}-1)s^{2}_{2}}{n_{1}+n_{2}-2}}\sqrt{ \frac{1}{n_{1}}+\frac{1}{n_{2}} }} \\
= \frac{(4.1-4.5)-(0)}{\sqrt{ \frac{(35-1)1.8^{2}+(27-1)2^{2}}{35+27-2}}\sqrt{ \frac{1}{35}+\frac{1}{27}}} \\
=-0.827
\end{split}
$$
area from this equation is between 0.1 and 0.5. This is a two tailed test, so we double the area. $0.2 <p-value<1$. This value is extremely high, so we do not reject $H_{0}$.

$\sigma$ is now assumed to be unequal. 
$df$ is calculated as
$$
\frac{\left( \frac{s^{2}_{1}}{n_{1}}+\frac{s^{2}_{2}}{n_{2}} \right)^{2}}{\frac{\left( \frac{s^{2}_{1}}{n_{1}} \right)^{2}}{n_{1}-1}+\frac{\left( \frac{s^{2}_{2}}{n_{2}} \right)^{2}}{n_{2}-1}}
$$
**Round down** to nearest integer. Usually, this is near to $n_{1}+n_{2}-2$.
Standard deviation is 
$$
s_{\bar{y}_{1}-\bar{y}_{2}} = \sqrt{ \frac{s^{2}_{1}}{n_{1}}+\frac{s^{2}_{2}}{n_{2}} }
$$
Test statistic is 
$$
t_{0}=\frac{(\bar{y}_{1}-\bar{y}_{2})-(\mu_{1}-\mu_{2})}{\sqrt{ \frac{s^{2}_{1}}{n_{1}}+\frac{s^{2}_{2}}{n_{2}}}}
$$
confidence interval is 
$$
=(\bar{y}_{1}-\bar{y_{2}})\pm t_{df, \alpha / 2}\sqrt{ \frac{s^{2}_{1}}{n_{1}}+\frac{s^{2}_{2}}{n_{2}} }
$$

Ex: We sampled 8 of the best passing offenses  and 8 of the best rushing offenses. Are QBs from passing offenses more effective passers?
$n_{1}$ = 8, $n_{2}$ = 8, $s_{1}$ = 4.303, $s_{2}$ = 4.637 $H_{0}:\mu_{1} \leq \mu_{2}$. The variances are close enough together that we could assume equal variances. 
$$
\begin{split}
t_{0} = \frac{(\bar{y}_{1}-\bar{y}_{2}) - 0}{\sqrt{ \frac{(n_{1}-1)s^{2}_{1}+(n_{2}-1)s^{2}_{2}}{n_{1}+n_{2}-2}}\sqrt{ \frac{1}{n_{1}}+\frac{1}{n_{2}} }} \\
= \frac{69.1-61.9}{\sqrt{ \frac{(8-1)4.3^{2}+(8-1)4.6^{2}}{8+8-2}}\sqrt{ \frac{1}{8}+\frac{1}{8} }} \\
t_{0} = 3.234
\end{split}
$$
3.234 results in a very small p-value which would be smaller than any reasonable p-value we can test for, so we reject $H_{0}$.

# Paired Samples
In some situations, two samples are taken from the same source, or from two otherwise dependent fashion. This are kind of like before-after kind of test. eg. productivity of an operator before and after a training course, the grades of a student before and after tutoring. 
Where $\bar{d}$ is the difference in the sample means. 
$$
t_{0} = \frac{\bar{d}-D_{0}}{s_{d}/\sqrt{ n }}
$$

Ex: we collect a sample of 12 operators, and we measure how long assembly takes using the standard approach and then we measure how long it takes with the new approach. Is the new approach better than the old one? $H_{0}:\mu_{d}\leq 0$. $\bar{d}$ = 4.833,$s_{d}$ = 1.764, $n$ = 12, $\alpha$ = 0.05.
$$
\begin{split}
t_{0} &= \frac{\bar{d}-D_{0}}{s_{d}/\sqrt{ n }} \\
&= \frac{4.833-0}{1.764/\sqrt{ 12 }} \\
t_{0} &= 9.56
\end{split}
$$
The biggest value in the t table on row 11 is 4.437, so the p-value is < 0.0005, so we reject $H_{0}$. The new approach is faster. From the t.dist.rt() function from excel $t_{0}$ = 5.784E-07.

Ex: We have some tasks that we want to know if automated systems are faster than a human system. $H_{0}:\mu_{d}\geq 0$, $\bar{d}$ = -32.56, $s_{d}$ = 35.03, $n$ = 8.
$$
\begin{split}
t_{0 }&= \frac{-32.56-0}{35.03/\sqrt{ 8 }} \\
t_{0} &= -2.629
\end{split}
$$
$t_{0.05,7}$ = -1.895. The test statistic is smaller than the critical value, so we reject $H_{0}$. The automated system is faster. 
# Proportions
$$
\begin{split}
\mu_{\hat{p}_{1}-\hat{p}_{1}} = p_{1} - p_{2} \\
\sigma_{\hat{p}_{1}-\hat{p}_{1}} = \sqrt{ \frac{\hat{p}_{1}(1-\hat{p}_{1})}{n_{1}} + \frac{\hat{p}_{2}(1-\hat{p}_{2})}{n_{2}}} \\
z_{0} = \frac{(\hat{p}_{1}-\hat{p_{2}}) - (p_{1}-p_{2})}{\sqrt{ \frac{\hat{p}_{1}(1-\hat{p}_{1})}{n_{1}} + \frac{\hat{p}_{2}(1-\hat{p}_{2})}{n_{2}}}}
\end{split}
$$
Ex: We have a sample of men and women and asked if they like soda from company A or B. We want to know if the proportion of women that like soda from A is significantly different from the proportion of men that like soda from A. $H_{0}:p_{1}-p_{2}=0$. $p_{m}$ = 0.606, $n_{m}$ = 66, $p_{w}$ = 0.511, $n_{w}$ = 184.
$$
\begin{split}
z_{0} &= \frac{(\hat{p}_{1}-\hat{p_{2}}) - (p_{1}-p_{2})}{\sqrt{ \frac{\hat{p}_{1}(1-\hat{p}_{1})}{n_{1}} + \frac{\hat{p}_{2}(1-\hat{p}_{2})}{n_{2}}}} \\
&= \frac{(0.511-0.606) - (0)}{\sqrt{ \frac{0.511(1-0.511)}{184} + \frac{0.606(1-0.606)}{66}}} \\
z_{0} &= -1.35
\end{split}
$$
The area from this test is 0.0885, but this is a two tailed test so we multiply this by 2. We get 0.177. This is a lot bigger than any reasonable confidence, so we don't reject $H_{0}$.

**Third exam material ends here**

# Difference in Variance
**F Distribution** - The ratio of $\chi$ variables $\frac{\chi_{1}/df_{1}}{\chi_{2}/df_{2}} \sim F_{df_{1},df_{2}}$
Test statistic:
$$
F_{0} = \frac{s^{2}_{1}}{s^{2}_{2}}
$$