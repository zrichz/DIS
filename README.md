### ONLY WORKS ON LINUX
### best resolution 1024x1024
## [Highly Accurate Dichotomous Image Segmentation （ECCV 2022）](https://arxiv.org/pdf/2203.03041.pdf) 

** (2022-Jul.-30)**  Thank [**AK391**](https://github.com/AK391) for the Web Demo:  [![Hugging Face Spaces](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue)](https://huggingface.co/spaces/doevent/dis-background-removal). <br> 

how to run: 
(1) Clone this repo
```
git clone https://github.com/xuebinqin/DIS.git
``` 
(2) Configuring the environment: go to the ```DIS/IS-Net``` folder and run 
```
conda env create -f pytorch18.yml
```
Or check the ```requirements.txt``` to configure dependencies. REMEMBER - LINUX ONLY
(3) activate the conda environment by 
```
conda activate pytorch18
``` 
(4) Inference
Download optimized model weights ```isnet-general-use.pth``` (for general use) from [(Google Drive)](https://drive.google.com/file/d/1nV57qKuy--d5u1yvkng9aXW1KS4sOpOi/view?usp=sharing) or [(Baidu Pan 提取码:6jh2)](https://pan.baidu.com/s/111MqmwnUc8Z4Wsq2Pc4bhQ?pwd=6jh2), and store them in ```saved_models/IS-Net``` <br>

(a) Open ```\ISNet\inference.py``` and configure your input and output directories
(b) Run 
```
python inference.py
```
