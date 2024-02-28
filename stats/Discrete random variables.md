**Reminder** - $${n \choose r}=\frac{n!}{(n-r)!r!}$$
# Binomial Probability Distribution
Describes when event $y$ happens when the experiment is repeated $n$ times. Each experiment is a Bernoulli trail for which there are only 2 outcomes. The probabilities of each outcome remain constant for each repetition, they are represented as $p$ and $1-p$. 

$Y$ = # of heads in $n$ = 5 coin flips. 
HHTTT $= pp(1-p)(1-p)(1-p)= p^2(1-p)^3$.
HTHTT$= p(1-p)p(1-p)(1-p) = p^2(1-p)^3$. 
There are $5 \choose 2$ ways to order 2 heads in 5 coin flips. 
When there are 2 heads, the probability can be described as: 
$$
\begin{split}
P(Y = 2) &={5 \choose 2}p^2(1-p)^3 \\
P(Y = 2) &= \frac{5!}{2!(5-2)!}(0.5)^2(0.5)^3 \\
P(Y = 2) &= 0.3125
\end{split}
$$
Equation: $$
P(Y=y)={n \choose y}p^y(1-p)^{n-y}
$$$Y$ = # of systems in 15 that operate
$n$ = 15, $p$ = 0.75. $P(Y=2)$.
$$
\begin{split}
P(Y=2)&={15 \choose 2}(0.75)^2(0.25)^{13}\\
P(Y = 2) &= \frac{15!}{2!(15-2)!}(0.75)^2(0.25)^{13} \\
P(Y = 2) &= 8.8\times 10^{-7}
\end{split}
$$
$P(6 \leq Y \leq 8) = P(Y=6) + P(Y=7) + P(Y=8)$.

**Expected Value** $\rightarrow$ $$
\begin{split}
E[Y]&=\sum_{i}y_{i}P(Y=y_{i})\\
&= \sum_{i}y_{i}{n \choose y_{i}}p^{y_{i}}(1-p)^{n-y_{i}} \\
&=np
\end{split}
$$
Expected value for the last problem: $E[Y] = 15(0.75) = 11.25$
$$
\begin{split}
J^2 &= E[y^2]-(E[y])^2 \\
&=
\end{split}
$$
There are 100 customer orders to fill. There is a 2% chance that a component is defective. If you stock 100 components, what is the probability that 100 order can be filled without reordering components?
$W$ = # of components in 100 that are defective. P(fill 100 orders). $P(W=0)$?
$$
\begin{split}
&= {100 \choose 0}(0.02)^0(0.98)^{100} \\
&= 0.133
\end{split}
$$
If there are 102 components are stocked, what is the probability that you can finish the 100 orders without ordering again now?
$W$ = # of components in 102 that are defective. $n$ = 102. $p$ = 0.02. We only need *at least* 100 components to work, having more than 100 working components is fine as well. So we add up all the probabilities together that satisfy us.
$$
\begin{split}
P(W\leq 2) = P(W=0)+P(W=1)+P(W=2) \\
= {102 \choose 0}(0.02)^0(0.98)^{102} + {102 \choose 1}(0.02)^1(0.98)^{102} + {102 \choose 2}(0.02)^2(0.98)^{102} \\
= \frac{2}{3}
\end{split}
$$If we bought only 5 more components, so 105 total parts. The probability that you can complete 100 orders is 0.9808. How nice.

# Hypergeometric Probability Distribution
The following is the equation to find the probability from a small sample size. A sample that is small enough to where the probability of each event is changed by the last event. **DO NOT GET HUNG UP ON REPLACEMENT AND NON-REPLACEMENT**.
$$
P(Y = y) = \frac{{r \choose y}{N - r \choose n - y}}{N \choose n}
$$
There is a committee of size 5 with a choice between 3 chemists and 6 physicist. If we count the chemists as bit of 1, then that would be that $r=3$ and that $N =9$. 
$$
\begin{split}
P(Y = 2) = \frac{{3 \choose 2}{6 \choose 3}}{9 \choose 5} 
\end{split}
$$
There are 75 washers. 5 of which have unacceptable variations. A sample of 10 is taken. 
$N=75$, $r = 5$, $n=10$, Y = # of unacceptable washers in 10. 
$$
P(Y = 0) = \frac{{5 \choose 0}{70 \choose 10}}{75 \choose 10} = 0.4786
$$
$P(Y \geq 1)$?
$$
P(Y \geq 1) = 1 - P(Y = 0) = 0.52142
$$
$P(Y=1)$?
$$
P(Y = 1) = \frac{{5 \choose 1}{70 \choose 9}}{75 \choose 10}
$$
Hypergeometric probability distribution 
$$
\mu = E[Y] = \frac{nr}{N}
$$
Electric components come in lots of 10. A purchaser randomly inspects 3 parts and he only buys the whole 10 if all 3 of sample are non-defective. This is called **Acceptance sampling**.
- If 30% of the lots have 4 defective components and the remaining 70% only have 1 defect, what proportion of the lots does he purchase?
A = supplier of 30% of lots w/ 4 defects. B = 70% of the lots w/ 1 defect. $Y_A$ = # of def comp in 10 from A. $Y_B$ = # of def comp in 10 from B. 
$P(accept \; a \; lot \mid A) = P(Y_{A} = 0)$. $$P(Y_{A} = 0) =\frac{{4 \choose 0}{6 \choose 3}}{10 \choose 3} = 0.167$$
$P(accept \; a \; lot \mid B) = P(Y_{B} = 0)$.  
$$
P(Y_{B} = 0) = \frac{{1 \choose 0}{9 \choose 3}}{10 \choose 3} = 0.7
$$

$$
\begin{split}
P(accept) = P(accept \mid A)P(A) + P(accept\mid B)P(B) \\
= (0.167)(0.3) + (0.7)(0.7) = 0.54
\end{split}
$$
# Poisson distribution
$\lambda$ = mean number of occurrences in that interval. $e$ = Euler
$$
P(Y=y) = \frac{\lambda ^{y}e^{-\lambda}}{y!}
$$
Bank customers arrive randomly on weekday afternoons at an average of 3.2 customers every 4 minutes. 
- What is the probability of having more than seven customers in a four minute interval on a weekday afternoon?
Y = # of customers arriving in 4 min. $\lambda$ = 3.2 $\frac{customers}{4 \; min}$. $P(Y > 7) =P(Y = 8) +P(Y =9) +P(Y =10) + \dots = 1 - P(Y \leq 7) = 1-[P(Y = 0) + \dots + P(Y=7)]$$$
1 - \left[ \frac{{3.2^0e^{-3.2}}}{0!} + \dots + \frac{{3.2^7e^{-3.2}}}{7!}\right]
$$There where 9 accidents in 3 years
 - What is the probability that an accident will happen next month?
 - What is the probability that an accident will happen in the next three months?

Y$ = # of accidents in a month. $\lambda$ = 9 accidents / 3 years = 1/4 accident / month. 
$$
P(Y=0) = \frac{{\lambda^y e^{-\lambda}}}{y!} = \frac{0.25^0 e^{-0.25}}{0!}= 0.779
$$
$X$ = # of accidents in 3 months. $\lambda$ = 1/4 accidents/ month = 3/4 accidents / 3 months
$$
\begin{split}
P(X \leq 2) = P(X = 0) + P(X = 1) + P(X = 2) \\
= \frac{0.75^0 e^{-0.75}}{0!} + \frac{0.75^0 e^{-0.75}}{1!} + \frac{0.75^0 e^{-0.75}}{2!}
\end{split}
$$
# Exponential Distribution
Distribution = $\lambda^{-\lambda y}$
Suppose that the time between injuries has an exponential distribution with a mean of 10 days
- What is the probability that the time between two consecutive injuries is less than 5 days?
$Y$ = time between injuries. $E[Y]=\mu$ = 10 days -> $\lambda=\frac{1}{\mu} =\frac{1}{10}=0.1$ injury per day. $P(Y<5)$?
$$
\begin{split}
P(Y<5) = \int ^5_{0}\lambda e^{-\lambda y} \, dy\\
F(5) = 1-e^{-\lambda y}=1-e^{-0.1(5)} \\
=0.393 \\
P(Y>10) = \int^\infty_{10}\lambda e^{-\lambda y} \, dy = 1 - F(10)\\
1-F(10) = 1-[1-e^{-0.1(10)}]\\
=0.368
\end{split}
$$
$Y$ = time to assemble module
$$
P(30<Y<35)=\int ^{35}_{30} \frac{1}{12}\, dy = \frac{{35-30}}{12}=.417 
$$
There is one call every 20 minutes before 10 AM. Arrival of calls follow a Poisson distribution. 
- What is the probability that at least one hour elapses between calls? (**THIS IS AN EXPONENTIAL DISTRIBUTION BECAUSE ITS TALKING ABOUT TIME BETWEEN CALLS**)
- What is the probability that 10 to 30 minutes elapses between calls?
$$
\begin{split}
P(Y>60) = 1 - F(60) = 1 - [1 - e^{-0.05(60)}]=e^{0.3} = 0.0497 \\
P(10<Y<30) = F(30) - F(10) = [1-e^{-0.05(30)}]-[1-e^{-0.05(10)}] = 0.383
\end{split}
$$
The average mpg is 20. A car uses 750 gallons of gasoline a year. If annual automobile usage is normally distributed, and if 29.12% of cars in the US use less than 500 gallons a year, what is the standard distribution?
$\sigma$ = 454.5 gallons