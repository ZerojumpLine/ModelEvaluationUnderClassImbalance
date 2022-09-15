## Requirements

```
pytorch==1.10.0
scipy==1.8.0
nibabel==3.2.2
pandas==1.3.5
numpy==1.21.2
seaborn=0.11.2
```

## Introduction

It is difficult for the practitioner to assess the model reliability on the target domain as labeled data for a new test domain is usually not available. It would be of great practical value to develop a tool to estimate the performance of a trained model on an unseen test domain without access to ground truth.

In this study we aim to estimate the model performance by only making use of unlabeled test data from the target domain.

<br/> <div align=center><img src="figs/introfig.png" width="700px"/></div>

We find existing methods struggle with data that present class imbalance, because the methods used to calibrate confidence do not account for bias induced by class imbalance, consequently failing to estimate class-wise accuracy. Here, we introduce class-wise calibration within the framework of performance estimation for imbalanced datasets.

<br/> <div align=center><img src="figs/Fig1_Motivation.png" width="700px"/></div>

## Data
Please download the data from [Data](https://drive.google.com/file/d/139pqxkG2ccIFq6qNArnFJWQ2by2Spbxt/view?usp=sharing), and put them under '/data/'.

## Model Evaluation on Classification task

Refer to juypter notebook:
```
ImbalanceCIFAR10.ipynb
```

## Model Evaluation on Segmentation task

Refer to jupyter notebook:
```
Prostate.ipynb
```

Note that the optimization process takes longer as we take probabiltiy maps as dense predictions.

We just show a result of one condition for simplicity. Please contact us (zeju.li18@imperial.ac.uk) for raw data if you want to reproduce more results in this paper.

## Citation
If you find our work has positively influenced your projects, please kindly consider to cite our work:

```
@article{li2022estimating,
  title={Estimating Model Performance under Domain Shifts with Class-Specific Confidence Scores},
  author={Li, Zeju and Kamnitsas, Konstantinos and Islam, Mobarakol and Chen, Chen and Glocker, Ben},
  journal={arXiv preprint arXiv:2207.09957},
  year={2022}
}
```