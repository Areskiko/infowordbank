# Words

## Important functions

$$
y = x + w

||x||^2 \leq NP
$$

## AWGN

The `AWGN` or `Additive White Gaussian Noise` is represented by a series of
output $Y$ with discrete time interval $i$. $X$ is the inputs and $Z$ is the
noise. The noise can also be denoted with $W$, as it is in the lectures.

Formula: $$Y_i = X_i + Z_i$$

### AWGN error

The probability of error when the number of _packets_ are large is:

$$ P_e = Q\left(\sqrt{\frac{||xQ function \_A - x_B||^2}{4\sigma^2}}\right) $$

Which is equal to:

$$ Q\left(\sqrt{\frac{NP}{\sigma^2}}\right) $$

$N$ is the number of messages (fact check this)

The [Q-function](https://en.wikipedia.org/wiki/Q-function), also known as
`Gaussian Q function` quantifies the probability of an error to exceed a certain
threshold.

## M-PAM repetition

TODO

## Repetition code problems

Repetition code packs every codeword into a single dimension whereas we have
multiple dimensions to use. The solution is to try to pack our N-dimensional
sphere some other way.

## Sphere packing

The goal of sphere packing is to maximize the number of codewords in the
available sphere. Any codeword has its own radius in which it interferes with
other codewords.
