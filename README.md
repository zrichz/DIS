### ONLY WORKS ON LINUX

## [Highly Accurate Dichotomous Image Segmentation （ECCV 2022）](https://arxiv.org/pdf/2203.03041.pdf) 

[**Project Page**](https://xuebinqin.github.io/dis/index.html), [**Arxiv**](https://arxiv.org/pdf/2203.03041.pdf), [**中文**](https://github.com/xuebinqin/xuebinqin.github.io/blob/main/ECCV2022_DIS_Chinese.pdf).

# Updates

** (2022-Aug.-17)** The optimized model for general use of our IS-Net is now released: ```isnet-general-use.pth``` (for general use) from [(Google Drive)](https://drive.google.com/file/d/1nV57qKuy--d5u1yvkng9aXW1KS4sOpOi/view?usp=sharing) or [(Baidu Pan 提取码:6jh2)](https://pan.baidu.com/s/111MqmwnUc8Z4Wsq2Pc4bhQ?pwd=6jh2), please feel free to try it with the newly created simple ```inference.py``` code on your own datasets.
![u2net-isnet-cmp]

** (2022-Jul.-30)**  Thank [**AK391**](https://github.com/AK391) for the Web Demo:  [![Hugging Face Spaces](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue)](https://huggingface.co/spaces/doevent/dis-background-removal). <br> 
## 6. Run Our Code

### (1) Clone this repo
```
git clone https://github.com/xuebinqin/DIS.git
``` 

### (2) Configuring the environment: go to the ```DIS/IS-Net``` folder and run 
```
conda env create -f pytorch18.yml
```
Or check the ```requirements.txt``` to configure dependencies. REMEMBER - LINUX ONLY

### (3) activate the conda environment by 
```
conda activate pytorch18
``` 
### (5) Inference
Download optimized model weights ```isnet-general-use.pth``` (for general use) from [(Google Drive)](https://drive.google.com/file/d/1nV57qKuy--d5u1yvkng9aXW1KS4sOpOi/view?usp=sharing) or [(Baidu Pan 提取码:6jh2)](https://pan.baidu.com/s/111MqmwnUc8Z4Wsq2Pc4bhQ?pwd=6jh2), and store them in ```saved_models/IS-Net``` <br>

## I. Simple inference code for your own dataset without ground truth:
(a) Open ```\ISNet\inference.py``` and configure your input and output directories
(b) Run 
```
python inference.py
```
