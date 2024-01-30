# Definitions
**Event** - The outcomes resulting from experiments
Probability Properties:
- Probability of an event has to lie between 0 and 1, \[0,1\]
- The sum of probabilities of all events of an experiment is *always* 1. 
**Classical Probability** - We have a more "absolute" notion of how to calculate probability. We know enough about a system to count the number of outcomes that occur and the number of ways event $A$ can occur.
*Ex*: event $A$: pick a winning lottery number. Experiment: a lottery with a 6 digit number.
$$P(A)=\frac{1}{10^6} = \frac{1}{1000000}$$ **Relative Frequency** - We use past history to extrapolate ideas about the occurrence of events.
$$P(A) = \frac{number \: of \: ways \: A \: has \: occured \: in \: the \: past}{total \: number \: of \: outcomes \: witnessed}$$
- Weather 
- Student passing rates
**Subjective Probability** - probability assigned to an event based on a subjective judgment.
- Sports gambling
**Marginal Probability** - The probability of an event occurring.
**Conditional Probability** - The probability of an event occurring on the condition of a second event happening. Written as $P(A\mid B)$.
**Mutually Exclusive** - Two or more events that can't happen at the same time. 
**Complementary Events** - The complement of event $A$. Written as $A^c$ or $A'$. $A^c$ is *everything but* $A$. $P(A) + P(A^c) = 1$.

**Union and Intersections** - Intersection ($\cap$) means "and".  Typically means multiply the probabilities together. Union($\cup$) means "or". Typically means to add the probability of the events together. $A \cup B = B \cup A$.
**Multiplication Rule** - If you have joint events $A$ and $B$, $P(A \cap B) = P(A\mid B)P(B)$. $P(B \cap A) = P(B \mid A)P(A)$. If events $A$ and $B$ are independent, $P(A \cap B) = P(A)P(B)$.

We have 2 factories, 10% from $A$ are defective and 18% from $B$ are defective. We would write that out as $P(D\mid A) = 0.1$ and $P(D \mid B) = 0.18$. The total amount that are defective would be $P(D) = P(D \mid A)P(A) + P(D \mid B)P(B)$ $=0.1(0.667)+0.18(0.333)$.

$P(A \mid B) + P(A' \mid B) = 1$ 

**Bayes Theorem** - $$P(A \mid B) = \frac{P(B \mid A)P(A)}{P(B)}$$ 
It rains 5 days of the year. The weatherman said it was going to rain tomorrow. Given that it does rain, the weatherman correctly predicts the weather 90% of the time. Given that it doesn't rain, the weatherman says that it will rain 5% of the time. So we would want $P(R \mid F)$. Event $F$ is the weatherman saying that it will rain.rainy days $R = \frac{5}{365}$. 
$P(F\mid R) = 0.9$ $P(F\mid R') = 0.05$. $$P(R \mid F)= \frac{P(F\mid R)P(R)}{P(F)}$$ We don't know $P(F)$, so we can find it using $P(F \mid R)P(R) + P(F \mid R')P(R')$.
$$P(R \mid F)= \frac{P(F\mid R)P(R)}{P(F \mid R)P(R) + P(F \mid R')P(R')}$$$$P(R \mid F)= \frac{(0.9)( \frac{5}{365})}{(0.9)( \frac{5}{365}) + (0.05)(\frac{360}{365})} = 0.2$$You have 500 components from A, 300 from B, and 200 from C. 200 from A are satisfactory, 150 were satisfactory from B, and 160 were satisfactory from C. If you pick a random satisfactory part, which factory is it most likely to come from? $S$ means a component is satisfactory. $P(A) =\frac{500}{1000}$, $P(B)=0.3$, $P(C) =0.2$. $P(S \mid A) =\frac{200}{500}=0.4$, $P(S \mid B) =\frac{150}{300}=0.5$, $P(S \mid C) =\frac{160}{200} = 0.8$. $P(S)$ is equal to $P(S \mid A)P(A) + P(S \mid B)P(B)+P(S\mid C)P(C)$. $$P(A \mid S)= \frac{P(S\mid A)P(A)}{P(S \mid A)P(A) + P(S \mid B)P(B)+P(S\mid C)P(C)}=0.392$$ $$P(B \mid S)= \frac{P(S\mid B)P(B)}{P(S)} = \frac{0.5(0.3)}{0.51}$$