# Word Bank for Information Theory

Or everything you need to know for the exam

- X -> Event
- P(X=i) or p_i -> probability of event i
- H(X) -> Entropy
- I(p) -> Information
- E(X) -> Expected value
- BR -> Bayes Rule

# Applications in Compression

> What is the minimum space needed for some information

## Information in Bits

A measure of the information content of an event

## Event - X

A stochastic variable `X` is a set of events which all have a chance of
occurring with some probability `p_i` for `i ∈ |X|` where `|X|` denotes the
cardinality of the alphabet (the number of events which may occur for the
stochastic variable)

## Shannon information - I(p)

`I(p)=-log_2(p)` gives the information in bits
`I(p)=-log_e(p)` gives the information in nats

## Entropy - H(X)

Entropy is defined as `H(X)=-∑p_i⋅log(p_i)` where `p_i` is the probability of
some event `i`, entropy is positive. In layman's terms it is the average
information of any event divided by the uncertainty

### Binary Entropy

For a binary stochastic variable `X` where `P(X=0)=p` and `P(X=1)=1-p` then
`H(X)=-p⋅log(p)-(1-p)⋅log(1-p)`, which is maximal with `p=0.5`

### Joint Entropy

The entropy for two discrete stochastic variables is given by
`H(X,Y) = -E[log(p(X,Y)] = -∑∑p(x,y)log(p(x,y))` where `E` is the expected
value. It is given that `H(X,Y) ≤ H(X)+H(Y)`

### Conditional Entropy

The entropy for one stochastic variable given another stochastic variable is
given by `H(X|Y) ≜ E[H(X|Y=y)] = -∑∑p(x|Y=y)⋅p(y)⋅log(p(x|Y=y))` which by
Bayes rule is `-∑∑p(x,y)⋅log(p(x,y)/p(y))`

# Applications in Communication

> How fast can we transmit data such that we do not lose information

## Signal to noise ratio - SNR

Signal divided by the noise
