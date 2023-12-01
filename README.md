# Broaden_your_view-image-mosaicking

[![Paper](https://img.shields.io/badge/paper-arXiv-green)](https://arxiv.org/abs/2311.13052)

This repository is the official implementation of [NOVEL OCT MOSAICKING PIPELINE WITH FEATURE- AND PIXEL-BASED REGISTRATION](https://arxiv.org/pdf/2311.13052.pdf). A novel OCT image mosaicking pipeline that bridges the gap between feature-based and pixel-based registration. We also investiage how to apply [SAM](https://segment-anything.com/) into the mosaicking evaluation pipeline.



## Prerequisite
- [LightGlue](https://github.com/cvg/LightGlue)
- [ANTs](https://github.com/ANTsX/ANTs)
- python==3.9.0
- monai==1.3.0
- openCV==4.8.1
- nibabel==5.1.0

## Synthetic OCTA-500
### OCTA-500 Data
Please check the original [paper](https://arxiv.org/pdf/2012.07261.pdf) and follow the steps specified in the IEEE [website](https://ieee-dataport.org/open-access/octa-500).
In our experiment, we only utilized the OCTA_6M data. We utilized monai to generate the known homography/affine transform and deform displacement. By this way, we can generate a synthetic dataset with known transform to evaluate the performance of the registration result. You can also implement it by `cv.Warp`; we also have the openCV implementation. 

Please check the full implementation `synthetic_octa-500.ipynb`


## Helper
To install ANTs on your desktop, I highly recommend you follow the great [tutorial](https://andysbrainbook.readthedocs.io/en/latest/ANTs/ANTs_Overview.html). This is designed for MAC, but it follows a similar installation logic for other UNIX systems. Please refer to the ANTs official Github to submit any [issues](https://github.com/ANTsX/ANTs/issues) regarding that.

## Reference
If you found this repo interesting, please check [our paper](https://arxiv.org/pdf/2311.13052.pdf)
```bibtex
@article{wang2023novel,
  title={Novel OCT mosaicking pipeline with Feature-and Pixel-based registration},
  author={Wang, Jiacheng and Li, Hao and Hu, Dewei and Tao, Yuankai K and Oguz, Ipek},
  journal={arXiv preprint arXiv:2311.13052},
  year={2023}
}
```

## Contact
Please contact Jiacheng Wang(jiacheng.wang.1@vanderbilt.edu) if you have any questions on the implementation or leave a issue.

##
