ENVIRONMENT SETUP

Make conda environment

conda create -n pytorch18 python=3.8
conda activate pytorch18

Install dependencies and clone the repository

git clone https://github.com/CeviKle/NTIRE2026-KLETech-CEVI-Denoising.git
cd NTIRE2026-KLETech-CEVI-Denoising

Install PyTorch

pip install torch==1.8.0+cu111 torchvision==0.9.0+cu111 torchaudio==0.8.0 -f https://download.pytorch.org/whl/torch_stable.html

Install required dependencies

pip install -r requirements.txt

Install BasicSR

python setup.py develop --no_cuda_ext

Download pretrained weights from the provided Google Drive link and place them in the **model_zoo** folder.

RUN TESTING

To run the test code for Gaussian color image denoising (σ = 50), use the following command:

python basicsr/test.py -opt options/test/test_swinir.yml
