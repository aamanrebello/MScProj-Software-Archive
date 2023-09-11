# Leveraging Factored Action Spaces for Off-Policy Evaluation - MSc Project Software Archive


Mathematical derivations were performed in the following scratchpad OverLeaf document: https://www.overleaf.com/read/hmxmjtkftvhv

The repo is arranged as follows:

- **Top Level**: 
Contains Python files used to run useful functions, which may also be used in the notebooks that implement experiments:

    - *policy_estimators.py*: Contains implementations of IS, PDIS, PDWIS and their non-factored equivalents. Also contains an on-policy estimator.

    - *load_discrete_MDP.py*:  Loads MDP 1 or MDP 2 into memory, based on information in **.configs/**. After loading, various MDP-related information is stored in variables e.g. non-factored and factored rewards, non-factored and factored policies, state abstraction-state mappings etc.

    - *load_datasets*: Contains a function to load data sets saved as npy files into memory. The data is stored in variables, containing different kinds of data i.e. factored or non-factored and generated from behaviour or evaluation policy.

    - *generate_dataset*: Runs simulations in MDP 1 or MDP 2 using the behaviour and evaluation policies and factored behaviour and evaluation policies specified in **.configs/** to generate datasets that are saved as *.npy* files in the **.datasets/** folder.

    - *discrete_MDP_helper_functions*: Contains useful functions used by the above four files and the experiment notebooks. The functions are used to process data loaded with *load_discrete_MDP.py* to derive new data.

