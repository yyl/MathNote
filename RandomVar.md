Random Variables
===

### Dicrete RV

***

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
    - `P_X(x) = sum_i_in_1-m(P_X|B_i(x)P[Bi]`, when `B` is an event space given as `Bi` where `i = 1, 2, ... m`
    - if `B` in `S_X` we have: `P_X|B(x) = P_X(x) / P[B]` if `x` in `B`, `0` if not
- conditional expected value
    - given condition `B`
    - `E[X|B] = u_X|B = sum_x_in_B(xP_X|B(x))`
    - when given enven space as condition, `B1, ..., B_m`
    - `E[X] = sum_i_in_1-m(E[X|B_i]P[B_i])
    
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

### Continuous RV

***

- _interval_: a continuous set of numbers containing all of the real numbers between two limits such as `(x1, x2)`
- `X` is continuous RV if its CDF `F_X(x)` is a continuous function
- example: voltage across a resistor
- probability density function (**PDF**)
    - `f_X(x) = dF_X(x) / dx`, given continuous RV `X`
    - the slope(derivative) of CDF: we use it to compute, say what is the probability of `x1 < X <= x2` (CDF)?
    - calculus talk: you have to give an interval to `f_X(x)` because the calculus of an exact single point is 0
        - say you want to know the probability of the amount of rain tomorrow equals exactly 2 inch, not 2.000000000001 or 1.9999999999999 inch 
        - the probability(CDF) is **0**!!
- expected value of a continuous RV `X`
    - `E[X] = int_-inf_inf( xf_X(x)dx )`
    - `E[g(X)] = int_-inf_inf( g(x)f_X(x)dx )`

#### Fuctions of a continuous RV

- derived RV
    - given `Y = aX`, then
        - CDF `F_Y(y) = F_X(y/a)`
        - PDF `f_Y(y) = (1/a)f_X(y/a)`

#### Families of continunous RV

- Uniform
- Exponential
- Erlang
- Gaussian
- Standard Normal
- Unit pulse (delta)
- Unit step
- Mixed

