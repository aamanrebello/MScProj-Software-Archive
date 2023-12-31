# Aaman Rebello (apr1718, 01488753) - MSc Project Software Archive

(Project title not written to prevent search conflicts with [this repo](https://github.com/ai4ai-lab/Factored-Action-Spaces-for-OPE))

Mathematical derivations were performed in the following scratchpad OverLeaf document: https://www.overleaf.com/read/hmxmjtkftvhv

The repo is arranged as follows:

- **Top Level**: 
Contains Python files used to run useful functions, which may also be used in the notebooks that implement experiments. Note that the experiment Jupyter notebooks in **./Notebooks** do not refer to this code but instead clone a [public repo](https://github.com/ai4ai-lab/Factored-Action-Spaces-for-OPE) which contains the exact same code files. Hence the notebooks can be run on their own in Google Colab, and have no dependencies.

    - *policy_estimators.py*: Contains implementations of IS, PDIS, PDWIS and their factored (decomposed) equivalents. Also contains an on-policy estimator. All estimators functions have similar interfaces.

    - *load_discrete_MDP.py*:  Loads MDP 1 or MDP 2 into memory, based on information in **./configs**. After loading, various MDP-related information is stored in variables e.g. non-factored and factored rewards, non-factored and factored policies, state abstraction-state mappings etc.

    - *load_datasets*: Contains a function to load data sets saved as npy files into memory. The data is stored in variables, containing different kinds of data i.e. factored or non-factored and generated from behaviour or evaluation policy.

    - *generate_dataset*: Runs simulations in MDP 1 or MDP 2 using the behaviour and evaluation policies and factored behaviour and evaluation policies specified in **.configs/** to generate datasets that are saved as *.npy* files in the **./datasets** folder.

    - *discrete_MDP_helper_functions*: Contains useful functions used by the above four files and the experiment notebooks. The functions are used to process data loaded with *load_discrete_MDP.py* to derive new data.
 
- **./Notebooks**: Contains the actual implementations of all the experiments in the project in JuPyter notebooks. Each notebook can be run on its own, without any dependencies, in [Google Colab](https://githubtocolab.com/aamanrebello/MScProj-Software-Archive). The notebooks are arranged into subfolders based on which chapter in the report their experiments are pertinent to. Descriptions of the notebooks in each of these subfolders are provided in a *Description.md* file.

- **./configs**:
  This contains the definitions of MDP's 1 and 2 in the form of csv and json files. There are two subfolders, one for MDP 1 and one for MDP 2. Each folder contains details on the non-factored MDP, as well as each of the MDP factors in subfolders. It also contains mappings from actions to factored actions, and states to state abstractions.

- **./datasets**: An empty folder used as a location to store data sets generated by *generate_dataset.py*.

- **./models**: Contains saved PyTorch models from neural network mapping experiments in Chapter 8 of the report. See *Description.md* within the folder for more information.
