# FALCON: Fair Active Learning using Multi-armed Bandits
Abstract: Biased data can lead to unfair machine learning models, emphasizing the need for incorporating fairness from the onset of data analysis, such as during dataset curation and labeling. We propose a scalable fair active learning framework, Falcon, that enhances machine learning model fairness via strategic sample selection. Given a user-specified group fairness measure, Falcon identifies samples from “target groups” (e.g., (attribute=female, label=positive)) that are the most informative for improving fairness. However, a challenge arises since these target groups are defined using ground truth labels that are not available during sample selection. To handle this, we propose a novel trial-and-error method, where we postpone using a sample if the predicted label is different from the expected one and falls outside the target group. We also observe the trade-off that selecting more informative samples results in higher likelihood of postponing due to undesired label prediction, and the optimal balance varies per dataset. We capture the trade-off between informativeness and postpone rate as policies and propose to automatically select the best policy using adversarial multi-armed bandit methods, given their computational efficiency and theoretical guarantees. Experiments show that Falcon significantly outperforms existing fair active learning approaches in terms of fairness and accuracy and is more efficient. In particular, only Falcon supports a proper trade-off between accuracy and fairness where its maximum fairness score is 1.8–4.5x higher than the second-best results.

## Setup

### Requirements
Create a conda environment (python=3.8.11) and install with ```setup.sh```.

#### Manual installation
We can also manually install the following packages with pip and conda.
```python
conda install jupyter
conda install scikit-learn
conda install -c conda-forge aif360
pip install folktables
```

### Datasets
<!-- You also need to manually install the COMPAS dataset from IBM’s AI Fairness 360 toolkit: https://github.com/Trusted-AI/AIF360. -->
Download and pre-process the datasets using IBM’s AI Fairness 360 toolkit: https://github.com/Trusted-AI/AIF360.

Folktables: https://github.com/socialfoundations/folktables

### Demos
To reproduce our experiments, please use the jupyter notebooks in the ```demos``` directory.
* ```Baseline_Comparison.ipynb```:
* ```Single_Policy_Baseline_Comparison.ipynb```:
