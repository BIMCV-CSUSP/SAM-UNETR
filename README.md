

# BIMCV-SAM-UNETR

This repository contains the code of SAM-UNETR, a model that combines the [Segment Anything Model (SAM)](https://github.com/facebookresearch/segment-anything) image encoder from Meta AI with a convolutional-decoder based on UNETR. SAM-UNETR was specifically trained and evaluated for the challenging task of Clinically Significant Prostate Cancer Segmentation.

![PI-RADS](images/PIR.png)

## Model Architecture

SAM-UNETR is designed to leverage the strengths of both SAM and UNETR to achieve accurate prostate cancer segmentation. The model incorporates the powerful image encoding capabilities of SAM with the effective convolutional-decoder structure of UNETR, resulting in improved segmentation performance.

![SAM-UNETR](images/SAMUNETR.png)
## Dataset

To train and evaluate SAM-UNETR, a dataset of clinically significant prostate cancer images was used. The dataset consists of high-resolution MRI scans along with corresponding ground truth segmentation masks from [PI-CAI Challenge](https://github.com/facebookresearch/segment-anything) and [Prostate158](https://github.com/kbressem/prostate158).

## Results

SAM-UNETR achieved good results on the Clinically Significant Prostate Cancer Segmentation task. The model's performance was evaluated against other models apliying the same technique.

![AUROC](images/ROC_Curve.png)

## Usage

To use SAM-UNETR first run [Extract_SAM_encoder_weigths.ipynb](Extract_SAM_encoder_weigths.ipynb) to save the weights of the image encoder, then run  requires `Train_model.py`  file that you want to use.
Finally `Analize_Results_model.py` contains the codes for predictions on each model

## Citing BIMCV-SAM-UNETR

BIMCV-SAM-UNETR is research software, made by a team of UMIB-FISABIO researchers. Citations and use of our software help us justify the effort which has gone into, and will keep going into, maintaining and growing this project.
If you have used BIMCV-SAM-UNETR in your research, please consider citing us:

> Alzate-Grisales, J. A., Mora-Rubio, A., García-García, F., Tabares-Soto, R., & De La Iglesia-Vayá, M. (2023). SAM-UNETR: Clinically Significant Prostate Cancer Segmentation Using Transfer Learning From Large Model.
> _IEEE Access_, 11, 118217-118228.
> https://ieeexplore.ieee.org/abstract/document/10292632

Or with BibTex:
```bibtex
@article{alzate2023sam,
  title={SAM-UNETR: Clinically Significant Prostate Cancer Segmentation Using Transfer Learning From Large Model},
  author={Alzate-Grisales, Jesus Alejandro and Mora-Rubio, Alejandro and Garcia-Garcia, Francisco and Tabares-Soto, Reinel and De La Iglesia-Vaya, Maria},
  journal={IEEE Access},
  volume={11},
  pages={118217--118228},
  year={2023},
  publisher={IEEE}
}
```
## Grants and funding
 
Funded by the Spanish Ministry of Economic Affairs and Digital Transformation (Project MIA.2021.M02.0005 TARTAGLIA, from the Recovery, Resilience, and Transformation Plan financed by the European Union through Next Generation EU funds). TARTAGLIA takes place under the R&D Missions in Artificial Intelligence program, which is part of the Spain Digital 2025 Agenda and the Spanish National Artificial Intelligence Strategy.
