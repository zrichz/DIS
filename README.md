## [Highly Accurate Dichotomous Image Segmentation （ECCV 2022）](https://arxiv.org/pdf/2203.03041.pdf) 

[**Project Page**](https://xuebinqin.github.io/dis/index.html), [**Arxiv**](https://arxiv.org/pdf/2203.03041.pdf), [**中文**](https://github.com/xuebinqin/xuebinqin.github.io/blob/main/ECCV2022_DIS_Chinese.pdf).

# Updates

** (2022-Aug.-17)** The optimized model for general use of our IS-Net is now released: ```isnet-general-use.pth``` (for general use) from [(Google Drive)](https://drive.google.com/file/d/1nV57qKuy--d5u1yvkng9aXW1KS4sOpOi/view?usp=sharing) or [(Baidu Pan 提取码:6jh2)](https://pan.baidu.com/s/111MqmwnUc8Z4Wsq2Pc4bhQ?pwd=6jh2), please feel free to try it with the newly created simple ```inference.py``` code on your own datasets.
![u2net-isnet-cmp](figures/u2net-isnet-cmp.png)

** (2022-Jul.-30)**  Thank [**AK391**](https://github.com/AK391) for the implementaiton of a Web Demo: Integrated into [Huggingface Spaces 🤗](https://huggingface.co/spaces) using [Gradio](https://github.com/gradio-app/gradio). Try out the Web Demo [![Hugging Face Spaces](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue)](https://huggingface.co/spaces/doevent/dis-background-removal). <br> 
## 6. Run Our Code

<br>

### (1) Clone this repo
```
git clone https://github.com/xuebinqin/DIS.git
``` 

### (2) Configuring the environment: go to the ```DIS/IS-Net``` folder and run 
```
conda env create -f pytorch18.yml
```
Or you can check the ```requirements.txt``` to configure the dependancies. 

### (3) activate the conda environment by 
```
conda activate pytorch18
``` 

### (4) Train:
(a) Open ```train_valid_inference_main.py```, set the path of your to-be-inferenced ```train_datasets``` and ```valid_datasets```, e.g., ```valid_datasets=[dataset_vd]``` <br>
(b) Set the ```hypar["mode"]``` to ```"train"``` <br>
(c) Create a new folder ```your_model_weights``` in the directory ```saved_models``` and set it as the ```hypar["model_path"] ="../saved_models/your_model_weights"``` and make sure ```hypar["valid_out_dir"]```(line 668) is set to ```""```, otherwise the prediction maps of the validation stage will be saved to that directory, which will slow the training speed down <br>
(d) Run 
```
python train_valid_inference_main.py
```

### (5) Inference

Download the pre-trained weights (for fair academic comparisons) ```isnet.pth``` from [(Google Drive)](https://drive.google.com/file/d/1KyMpRjewZdyYfxHPYcd-ZbanIXtin0Sn/view?usp=sharing) or [(Baidu Pan 提取码：xbfk)](https://pan.baidu.com/s/1-X2WutiBkWPt-oakuvZ10w?pwd=xbfk) OR the optimized model weights ```isnet-general-use.pth``` (for general use) from [(Google Drive)](https://drive.google.com/file/d/1nV57qKuy--d5u1yvkng9aXW1KS4sOpOi/view?usp=sharing) or [(Baidu Pan 提取码:6jh2)](https://pan.baidu.com/s/111MqmwnUc8Z4Wsq2Pc4bhQ?pwd=6jh2), and store them in ```saved_models/IS-Net``` <br>

## I. Simple inference code for your own dataset without ground truth:
(a) Open ```\ISNet\inference.py``` and configure your input and output directories
(b) Run 
```
python inference.py
```

