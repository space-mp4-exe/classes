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
$$$$
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
