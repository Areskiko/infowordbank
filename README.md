# Word Bank for Information Theory

Or everything you need to know for the exam

- X -> Event
- P(X=i) or p_i -> probability of event i
- H(X) -> Entropy
- I(p) -> Information
- E(X) -> Expected value
- BR -> Bayes Rule
- D(p||q) -> Informational distance

# Applications in Compression

What is the minimum space needed for some information

## Information in Bits

A measure of the information content of an event

## Event - X

A stochastic variable $X$ is a set of events which all have a chance of
occurring with some probability $p_{i}$ for $i\in|X|$ where $|X|$ denotes the
cardinality of the alphabet (the number of events which may occur for the
stochastic variable)

## Shannon information - I(p)

- $I(p)=-log_2(p)$ gives the information in bits
- $I(p)=-log_e(p)$ gives the information in nats

## Entropy - H(X)

Entropy is defined as
$$H(X)=-\sum_{i=1}^{|X|}p_i\cdot log(p_i)$$

Where $p_i$ is the probability of some event $i$, entropy is positive. In
layman's terms it is the average information of any event divided by the
uncertainty

### Binary Entropy

For a binary stochastic variable $X$ where $P(X=0)=p$ and $P(X=1)=1-p$ then
$$H(X)=-p\cdot log(p)-(1-p)\cdot log(1-p)$$

Which is maximal with $p=0.5$

### Joint Entropy - H(X,Y)

The entropy for two discrete stochastic variables is given by
$$H(X,Y)=-E[log(p(X,Y)]=-\sum_{x\in X}\sum_{y\in Y}p(x,y)log(p(x,y))$$

Where $E$ is the expected value

It is given that $H(X,Y)\leq H(X)+H(Y)$

### Conditional Entropy - H(X|Y)

The entropy for one stochastic variable given another stochastic variable is
given by
$$H(X|Y)\triangleq E[H(X|Y=y)]=-\sum_{x\in X}\sum_{y\in Y} p(x|Y=y)\cdot p(y)\cdot log(p(x|Y=y))$$

Which by Bayes rule is
$$-\sum_{x\in X}\sum_{y\in Y}p(x,y)\cdot log\left(\frac{p(x,y)}{p(y)}\right)$$

It is given that $H(X|Y)\leq H(X)$

### Mutual Information - I(X;Y)

The mutual information between two stochastic variables is given by
$$I(X;Y)=H(X)-H(X|Y)=H(Y)-H(Y|X)=H(X)+H(Y)-H(X,Y)$$

If $I(X;Y)=0$ then $X$ and $Y$ are independent

### Chain Rule

There exists two chain rules

#### Entropy chain rule

$$H(X,Y)=H(Y)+H(X|Y)=H(Y,X)=H(X)+H(Y|X)$$

More generally

$$H(X1,X2,...,Xn)=H(X1)+H(X2|X1)+H(X3|X1,X2)+...+H(Xn|X1,X2,...,Xn-1)$$

#### Information chain rule

$$I(X,Y;Z)=I(X;Z)+I(Y;Z|X)$$
which gives rise to the conditional mutual information

$$I(Y;Z|X)=H(Y|X)-H(Y|Z,X)$$

### Relative entropy - D(p||q)

The information distance
$$D(p||q)=\sum{x\in X}p(x)\cdot log\left(\frac{p(x)}{q(x)}\right)$$
$$D(p||q)=E_{p(X)}[log(p(X))-log(q(X)]$$

Measures the degree of independence between $X$ and $Y$

$$D(p(X,Y)||p(X)p(Y))=I(X;Y)$$

### Maximal entropy

We always have that

$$H(X)\leq log(|X|)$$

With equality if $X$ is evenly distributed, which means that uniform
distribution maximizes entropy

## Jensen's inequality

For a convex function (sagging or u-shaped) we have that

$$E[f(X)]\geq f(E[X])$$

For a concave function we have that

$$E[f(X)]\leq f(E[X])$$

## Data Processing Inequality

TODO

# Applications in Communication

> How fast can we transmit data such that we do not lose information

## Signal to noise ratio - SNR

Signal divided by the noise
