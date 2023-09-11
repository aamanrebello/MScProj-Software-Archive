# Chapter 8
Investigates different ways to learn an action space factorisation and/or quantities derived from these.

Description of notebooks:

- **Constrained_Factor_Optimisation**: This contains an attempt to optimise the factored policies and rewards in the IS estimator with the help of the *SciPy* `minimize` function. This attempt was eventually abandoned because it was too difficult to optimise over 20,000 parameters.

- **Clustering_Factors**: This clusters actions based on the independent changes they induce in the state features. Based on this, a new action space factorisation is derived, which is tested on the Sepsis Simulator.

- **Clustering_Method_Graphs**: This plots graphs of PDIS and IS, using the factorisation learned from the clustering approach, against PDIS/IS with other factorisations based on action features. It also plots the estiamation bias of the former factorisation for different levels of policy divergence, and plots policy approximation error graphs.

- **NN_Based_Factor_Optimisation**: This trains neural networks to map (s,a) pairs or ($\pi_b(s,a)$, $\pi_e(s,a)$, $r(s,a)$) to their corresponding set of policy and reward factors. This file contains the learning curve graphs.

- **Test_NN_Factors**: This tests different models trained to perform the neural network mapping approach on various data sets and plots graphs.

- **Policy_Factorisation_Error**: Analyses the approximation error resulting from imperfect policy factorisation of an $\epsilon$-greedy policy.