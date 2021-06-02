# FaceScape

*FaceScape* provides large-scale high-quality 3D face datasets, parametric models, docs and toolkits about 3D face related technology. [[CVPR2020 paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Yang_FaceScape_A_Large-Scale_High_Quality_3D_Face_Dataset_and_Detailed_CVPR_2020_paper.pdf) &nbsp;&nbsp; [[supplemetary]](https://openaccess.thecvf.com/content_CVPR_2020/supplemental/Yang_FaceScape_A_Large-Scale_CVPR_2020_supplemental.zip)

Our latest progress will be updated to this repository constantly - *[latest update: 2021/4/14]*

```diff
- We are very sorry that due to the renovation of the campus network, the FaceScape website (https://facescape.nju.edu.cn/)
- is temporarily inaccessible. The service will resume after 24:00PM, June 10, 2021. 
```

### Data

The data can be downloaded in https://facescape.nju.edu.cn/ after requesting a license key.
*New:* The bilinear model ver1.6 can be downloaded without requesting a license key, view [here](https://github.com/zhuhao-nju/facescape/blob/master/doc/external_link_fsbm.md) for the link and rules.

<img src="/figures/facescape_all.jpg" width="800"> 

The available sources include:

| Item              | Description                                                         | Quantity                                         | Quality |
|-------------------|---------------------------------------------------------------------|------------------------------------------------|---------|
| TU models | Topologically uniformed 3D face models <br>with displacement map and texture map. | **16940 models** <br>(847 id × 20 exp)       |  Detailed geometry, <br>4K dp/tex maps |
| Multi-view data | Multi-view images, camera paramters <br>and coresponding 3D face mesh. | **>400k images** <br>(359 id × 20 exp <br>× ≈60 view)|  4M~12M pixels       |
| Bilinear model | The statistical model to transform the base <br>shape into the vector space.  |   4 for different settings      |    Only for base shape.    |
| Info list         | Gender / age of the subjects.                                        |   847 subjects   |    --    |
 
The datasets are only released for non-commercial research use.  As facial data involves the privacy of participants, we use strict license terms to ensure that the dataset is not abused.

### Docs
* [doc of TU models](/doc/doc_tu_model.md).
* [doc of Multi-view models](/doc/doc_mview_model.md).
* [doc of Bilinear models](/doc/doc_bilinear_model.md).

### ToolKit
Start using python toolkit [here](/toolkit/README.md), the demos include:

* [bilinear_model-basic](https://nbviewer.jupyter.org/github/zhuhao-nju/facescape/blob/master/toolkit/demo_bilinear_basic.ipynb) - use facescape bilinear model to generate 3D mesh models.
* [bilinear_model-fit](https://nbviewer.jupyter.org/github/zhuhao-nju/facescape/blob/master/toolkit/demo_bilinear_fit.ipynb) - fit the bilinear model to 2D/3D landmarks.
* [multi-view-project](https://nbviewer.jupyter.org/github/zhuhao-nju/facescape/blob/master/toolkit/demo_mview_projection.ipynb) - Project 3D models to multi-view images.
* [landmark](https://nbviewer.jupyter.org/github/zhuhao-nju/facescape/blob/master/toolkit/demo_landmark.ipynb) - extract landmarks using predefined vertex index.
* [facial_mask](https://nbviewer.jupyter.org/github/zhuhao-nju/facescape/blob/master/toolkit/demo_mask.ipynb) - extract facial region from the full head TU-models.
* [render](https://nbviewer.jupyter.org/github/zhuhao-nju/facescape/blob/master/toolkit/demo_render.ipynb) - render TU-models to color images and depth map. 
* [alignment](https://nbviewer.jupyter.org/github/zhuhao-nju/facescape/blob/master/toolkit/demo_align.ipynb) - align all the multi-view models.
* [symmetry](https://nbviewer.jupyter.org/github/zhuhao-nju/facescape/blob/master/toolkit/demo_symmetry.ipynb) - get the correspondence of the vertices on TU-models from left side to right side.
* rigging (Coming soon) - rig the TU-models to an simple animation with changing experssions.
 
### Code
The code of detailed riggable 3D face prediction in our paper is released [here](https://github.com/yanght321/Detailed3DFace.git).

### ChangeLog
* **2021/5/13** <br>
Fitting demo is added to toolkit. Please note if you download bilinear model v1.6 before 2021/5/13, you need to download it again, because some parameters required by fitting demo are supplemented.
* **2021/4/14** <br>
The bilinear model has been updated to 1.6, check it [here](/doc/doc_bilinear_model.md).<br>
The new bilinear model now can be downloaded from *NJU drive* or *Google Drive* without requesting a license key. Check it [here](/doc/external_link_fsbm.md).<br>
ToolKit and Doc has been updated with new content.<br>
Some wrong ages and genders in the info list are corrected in "info_list_v2.txt".<br>
* **2020/9/27** <br>
The code of detailed riggable 3D face prediction is released, check it [here](https://github.com/yanght321/Detailed3DFace.git).<br>
* **2020/7/25** <br>
Multi-view data is available for download.<br>
Bilinear model is updated to ver 1.3, with vertex-color added.<br>
Info list including gender and age is available in download page.<br>
Tools and samples are added to this repository.<br>
* **2020/7/7** <br>
Bilinear model is updated to ver 1.2. 
* **2020/6/13** <br>
The [website]((https://facescape.nju.edu.cn/)) of FaceScape is online. <br>3D models and bilinear models are available for download.<br>
* **2020/3/31** <br>
The pre-print paper is available on [arXiv](https://arxiv.org/abs/2003.13989).<br>

### Bibtex
If you find this project helpful to your research, please consider citing:
```
@InProceedings{yang2020facescape,
  author = {Yang, Haotian and Zhu, Hao and Wang, Yanru and Huang, Mingkai and Shen, Qiu and Yang, Ruigang and Cao, Xun},
  title = {FaceScape: A Large-Scale High Quality 3D Face Dataset and Detailed Riggable 3D Face Prediction},
  booktitle = {IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
  month = {June},
  year = {2020},
  page = {601--610}}
```

### Acknowledge
The project is supported by [CITE Lab](https://cite.nju.edu.cn/) of Nanjing University, Baidu Research, and Aiqiyi Inc.  The student contributors: Ji Shengyu, Jin Wei, Huang Mingkai, Wang Yanru, Yang Haotian, Zhang Yidi, Xiao Yunze, Ding Yuxin, Guo Longwei.
