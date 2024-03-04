# ecole-branching-imitation-solver

## Branching with Imitation Learning and a GNN

A simplified version of the paper of Gasse et al. (2019) on learning to branch with Ecole with pytorch and pytorch geometric. We collect strong branching examples on randomly generated maximum set covering instances, then train a graph neural network with bipartite state encodings to imitate the expert by classification. Finally, we will evaluate the quality of the policy.

The biggest difference with Gasse et al. (2019) is that only n=1,000 training examples of expert decisions are collected for training, to keep the time needed to run the tutorial reasonable. As a consequence, the resulting policy is undertrained and is not competitive with SCIP's default branching rule.

Users that are interested in reproducing competitive performance should use a larger sample size, such as the n=100,000 samples used for training in the paper. In this case, we strongly recommend to parallelize data collection, as in the original Gasse et al. (2019) code.
