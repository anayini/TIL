# Branch Prediction

## Basics

Moderns CPUs tend to pipeline operations, which can lead to more efficiency.  This tends to become harder when taking branches, since we are unable to figure out what to push into the pipeline
without first evaluating the branch.  Branch prediction is a form of speculation where we guess the outcome of a branch and pipeline
work based on the predicted outcome.  In the case that we are correct, we gain some efficiency, in the case that we are wrong,
we did some needless work.  This can workout to be a net positive
if we have a good success rate in our prediction.

### Strategies

#### Static
1. Always take branch - Based on data, branches are taken more often then they are not, so this simple heuristic actually gives some performance gains.

#### Dynamic

Keep additional state to understand branch probabilities over time.

1. One bit - Keep a fixed size table indexed by last N bits of an
address that holds the last branch outcome for the branch at that address.  Always predict that the next value will be equal to the last value.
1. Two - same as the above but we can keep extra information about history.
1. N-Bit - same as above, but turns out to have pretty diminishing
returns for N>2.
