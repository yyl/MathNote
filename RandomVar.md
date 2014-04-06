Random Variables
===

A random variable `X` is the observation of 
### Dicrete RV

- random variable `X`: 
    - a variable whose possible values are numerical outcomes of a random phenomenon
    - `X` is observations of a _probability model_
    - a probability model is trying to define an _experiment_
    - an experiment has a procedure and a set of _observations_
    - the all possible observations of an experiment is its _sample space_
    - for every `A` in `S`, the model gives a probability `P[A]` that `0 <= P[A] <= 1`
- discrete RV: 
    - `X` may only take on a countable number of distinct values 
    - usually are _counts_
    - example: number of children in a family, attendance of a movie
- probability mass function (**PMF**)
    - `P_X(x) = P[X = x]`, given discrete random variable `X`,
    - `x` is a possible value of `X`
    - for any value of `x`, `P_X(x)` is the probability of the event `X = x`
- cumulative distribution function (**CDF**)
    - `F_X(x) = P[X <= x]`, given discrete RV `X`
    - for any real number `x`, CDF is the probability that `X` is no larger than `x` (cumulative)
    - correlated to _PMF_, each could be obtained from each other
    - properties
        - `F_X(-inf) = 0` and `F_X(inf) = 1`
        - CDF never decrease as it goes from left to right
        - `F_X(b) - F_X(a) = P[a < X <= b]`, given all `b >= a`
- expected value of `X`
    - `E[X] = u_X = sum_x_in_S(xP_X(x))`
    - `S` is the sample sapce of `X`
    - for any RV `X`,
        - `E[X - u_X] = 0`
        - `E[aX + b] = aE[X] + b`
- conditional PMF
    - given event `B` with `P[B] > 0`
    - `P_X|B(x) = P[X = x|B]`

#### Functions of a RV

- derived RV: `Y = g(X)`
    - each value `y` of a derived RV `Y` is a mathematical function `g(x)` of a value `x` of RV `X`
    - `P_Y(y) = sum_x:g(x)=y(P_X(x))`
    - `P[Y = y]` is the sum of probabilities of all outcomes `X = x` for which `Y = y`
- expected value of a derived RV
    - `E[Y] = sum_x_in_S(g(x)P_X(x))`, given `Y = g(X)`

#### Families of discrete RV

- Bernoulli
- Geometric
- Binomial
- Pascal
- Discrete uniform
- Poisson
