# [Differential Privacy: A Survey of Results](https://www.cell.com/patterns/fulltext/S2666-3899(21)00097-0)
## What should know

if the noise is symmetric about the originand the same question is asked many times, the responses may be averaged,cancelling out the noise. *and record queries to return same result is impossible in some ways* [Revealing Information While Preserving Privacy (2003)](https://dl.acm.org/doi/abs/10.1145/773153.773173)

scaled symmetric exponential distribution with standard deviation $\frac{√2\Delta f}{\epsilon}$ denoted $Lap\frac{\Delta f}{\epsilon}$


## Definition 1.

randomized function $\mathcal{K}$ gives-differential privacyif for alldata sets $D1$ and $D2$ differing on at most one element, and all $S⊆Range(\mathcal{K})$.

$$Pr[\mathcal{K}(D1)\in S]≤exp(\epsilon)×Pr[\mathcal{K}(D2)\in S]$$

## Remark 1
1. The parameter in Definition 1 is public. The choice of is essentially a social question and is beyond the scope of this paper. That said, wetend to think of as, say, 0.01, 0.1, or in some cases, ln 2 or ln 3. If the prob-ability that some bad event will occur is very small, it might be tolerable toincrease it by such factors as 2 or 3, while if the probability is already felt tobe close to unacceptable, thenan increase by a factor of $e^{0.1} \approx 1.01$ might betolerable, while an increase ofe,orevenonlye0.1, would be intolerable
2. Definition 1 discusses the behavior of the mechanism $K$, and is independent of any auxiliary knowledge the adversary, or user, may have about thedatabase. Thus, a mechanism satisfying the definition protects the privacyof an individual row in the database even if the adversary knows every otherrow in the database.
3. Definition 1 extends to group privacy as well (and to the case in which anindividual contributes more than a single row to the database). A collectionofcparticipants might be concerned that their collective data might leakinformation, even when a single participant’s does not. Using this definition,we can bound the dilation of any probability by at most $exp(\epsilon c)$, which maybe tolerable for smallc. Of course, the point of the statistical database isto disclose aggregate information about large groups (while simultaneouslyprotecting individuals), so we should expect privacy bounds to disintegratewith increasing group size.


## Definition 2
For $f:\mathcal{D}→R^k$, the sensitivity of $f$ is

$$Δf=\max\limits_{D1,D2}‖f(D1)−f(D2)‖_1$$
