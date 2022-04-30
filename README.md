# MoleculeNet

This repo is a fork version of actual [DGL-LIFESCI](https://github.com/awslabs/dgl-lifesci) repo. This has limited component and confiiguration to just test out GCN, GAT models on Tox21 and ToxCast Dataset.

[MoleculeNet](https://arxiv.org/abs/1703.00564) is a popular benchmark for molecular machine learning.
For validating the robustness of DGL-LifeSci, we report the results of applying the 
[command-line interface](../csv_data_configuration) against 12 datasets in MoleculeNet, including 
9 classification datasets (BACE, BBBP, ClinTox, HIV, MUV, PCBA, SIDER, Tox21 and ToxCast) and 
3 regression datasets (ESOL, FreeSolv and Lipophilicity). 

To train a model on a classification dataset, use 

```bash
python classification.py -d DATASET -mo MODEL -f FEATURE 
```

where:
- `DATASET` specifies the dataset for experiment, which can be one of  `ToxCast`, `Tox21`
- `MODEL` specifies the model to use, which can be one of `GCN`, `GAT
- `FEATURE ` specifies the featurization method to use, which can be one of `canonical`, 
  `attentivefp`.
