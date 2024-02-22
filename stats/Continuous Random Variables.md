Continuous numbers have an $\infty$ possible numbers. Think about regular numbers that go on the number line. Their distributions have to be represented with a line graph rather than a histogram. 
$UB$ - Upper bound, the highest value in the range. $LB$ - lower bound.
Expected value for *continuous* variables 
$$
E[Y] = \int^{UB}_{LB}yf(y) \, dy 
$$
Variance 
$$
\text{Var}[Y] = \int ^{UB}_{LB}y^2f(y)\, dy - (E[Y])^2
$$
Cumulative 
$$
P(Y \leq y) = \int ^y_{LB}f(t) \, dt 
$$
These are basically taking the integral of their density graphs to find the probability.
**You cant find a probability of a single point, it has to be a range**.
***
# Normal Distribution
*also called a gaussian distribution or bell curve*.
Mean - $\mu$, variance - $\sigma^2$
$$
f(y) = \frac{1}{\sigma \sqrt{ 2 \pi }}e^{-(1/2)[(y - \mu)/\sigma]^2}
$$
Probability for a particular interval \[a, b\]
$$
f(y) = \int^a_{b}\frac{1}{\sigma \sqrt{ 2 \pi }}e^{-(1/2)[(y - \mu)/\sigma]^2}\, dy
$$
Z score is found by normalizing the data
$$
Z = \frac{y-\mu}{\sigma}
$$