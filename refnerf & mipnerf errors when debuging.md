# issues when debug refnerf & mipnerf
## 官方代码multinerf
### 目前没有调通，问题出现在JAX，JAXlib版本和cuda，cudann冲突
## refnerf-pytorch/refnerf-pl版本调通过程
### Clone the repo.
git clone https://github.com/gkouros/refnerf-pytorch.git

或

git clone https://github.com/minfenli/refnerf-pl.git

cd refnerf-pytorch 或 cd refnerf-pl

### Make a conda environment.
conda create --name refnerf-pl python=3.9

conda activate refnerf-pl

~~pip3 install torch torchvision --extra-index-url https://download.pytorch.org/whl/cu116~~

pip3 install torch==1.12.1+cu116  torchvision==0.13.1+cu116 torchaudio==0.12.1 -f https://mirrors.aliyun.com/pytorch-wheels/cu116/

### Prepare pip.
conda install pip

pip install --upgrade pip

### Install requirements.
pip install -r requirements.txt

### Manually install rmbrualla's `pycolmap` (don't use pip's! It's different).
git clone https://github.com/rmbrualla/pycolmap.git ./internal/pycolmap

## 可能的报错信息
### 报错ModuleNotFoundError: No module named 'functorch'
pip install funtorch

### jax jaxlib使用cpu版本，如何切换到GPU版本
从下面的连接安装

https://storage.googleapis.com/jax-releases/jax_cuda_releases.html

jax jaxlib冲突问题
