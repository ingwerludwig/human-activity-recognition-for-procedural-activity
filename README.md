<div align="center">
  <img src="resources/mmdet-logo.png" width="600"/>
  <div>&nbsp;</div>
  <div align="center">
    <b><font size="5">OpenMMLab website</font></b>
    <sup>
      <a href="https://openmmlab.com">
        <i><font size="4">HOT</font></i>
      </a>
    </sup>
    &nbsp;&nbsp;&nbsp;&nbsp;
    <b><font size="5">OpenMMLab platform</font></b>
    <sup>
      <a href="https://platform.openmmlab.com">
        <i><font size="4">TRY IT OUT</font></i>
      </a>
    </sup>
  </div>
  <div>&nbsp;</div>

[![PyPI](https://img.shields.io/pypi/v/mmdet)](https://pypi.org/project/mmdet)
[![docs](https://img.shields.io/badge/docs-latest-blue)](https://mmdetection.readthedocs.io/en/latest/)
[![badge](https://github.com/open-mmlab/mmdetection/workflows/build/badge.svg)](https://github.com/open-mmlab/mmdetection/actions)
[![codecov](https://codecov.io/gh/open-mmlab/mmdetection/branch/main/graph/badge.svg)](https://codecov.io/gh/open-mmlab/mmdetection)
[![license](https://img.shields.io/github/license/open-mmlab/mmdetection.svg)](https://github.com/open-mmlab/mmdetection/blob/main/LICENSE)
[![open issues](https://isitmaintained.com/badge/open/open-mmlab/mmdetection.svg)](https://github.com/open-mmlab/mmdetection/issues)
[![issue resolution](https://isitmaintained.com/badge/resolution/open-mmlab/mmdetection.svg)](https://github.com/open-mmlab/mmdetection/issues)
[![Open in OpenXLab](https://cdn-static.openxlab.org.cn/app-center/openxlab_demo.svg)](https://openxlab.org.cn/apps?search=mmdet)
<!-- ABOUT THE PROJECT -->
## The Human Activity Recognition Project using Pytorch Framework
### Built With
* [![PyTorch][PyTorch]][PyTorch-url]
* [![Python][Python]][Python-url]
* [![nVIDIA][nVIDIA]][nVIDIA-url]


### Prerequisite
1. Python 3.8.15 Installed </br>
2. Create Conda Environment</br>
    ```sh
    conda create -n HAR-mmlab python=3.8.15
    ```
    ```sh
    conda activate HAR-mmlab
    ```
3. Linux OS (Ubuntu 20.04)

### Installation
_This is the installation guide for Setting Pytorch with CUDA GPU Support_

1. Install the NVIDIA GPU Driver 530.30.02

    ```sh
    wget https://developer.download.nvidia.com/compute/cuda/12.1.0/local_installers/cuda-repo-ubuntu2004-12-1-local_12.1.0-530.30.02-1_amd64.deb
    ```
    ```sh
    sudo dpkg -i cuda-repo-ubuntu2004-12-1-local_12.1.0-530.30.02-1_amd64.deb
    ```
    ```sh
    sudo cp /var/cuda-repo-ubuntu2004-12-1-local/cuda-*-keyring.gpg /usr/share/keyrings/
    ```
    ```sh
    sudo apt-get update
    ```
    ```sh
    sudo apt-get -y install cuda
    ```
2. Check the Installed GPU Driver Version (The installed NVIDIA Driver should be 530.30.02)
   ```sh
   modinfo nvidia
   ```
3. Reboot the computer </br>
4. Install the CUDA Toolkit 11.3 (supported with NVIDIA GPU Driver version)
    ```sh
    wget https://developer.download.nvidia.com/compute/cuda/11.3.0/local_installers/cuda_11.3.0_465.19.01_linux.run
    ```
    ```sh
    sudo sh cuda_11.3.0_465.19.01_linux.run
    ```
5. Check the installation except the NVIDIA Driver and replace the installed CUDA Toolkit
6. Export PATH for CUDA Toolkit
    ```sh
    echo ‘export PATH=/usr/local/cuda-11.3/bin:$PATH’ >> ~/.bashrc
    ```
    ```sh
    echo ‘export LD_LIBRARY_PATH=/usr/local/cuda-11.3/lib64:$LD_LIBRARY_PATH’ >> ~/.bashrc
    ```
7. Install all the selected files and reboot the computer
8. Check the NVIDIA Driver Toolkit Version
    ```sh
    nvidia-smi
    ```
9. Install the cuDNN
    ```sh
    conda install -c nvidia cuda-nvcc==11.3
    ```
   or
    ```sh
    conda install -c "nvidia/label/cuda-11.3.0" cuda-nvcc
    ```
10. Install PyTorch (Must be the exact same version with the CUDA Toolkit Version)
    ```sh
    pip install torch==1.10.2+cu113 torchvision==0.11.3+cu113 torchaudio==0.10.2+cu113 -f https://download.pytorch.org/whl/cu113/torch_stable.html

    ```
11. Verify GPU Support
    ```sh
    import torch
    print(torch.cuda.is_available())
    ```
12. Install all the required MM's library
    ```sh
    pip install mmengine==0.10.4
    ```
    ```sh
    pip install mmdet==3.3.0
    ```
    ```sh
    pip install mmcv==2.0.0rc4
    ```
13. Clone this project repository
    ```sh
    git clone https://github.com/ingwerludwig/human-activity-recognition-for-procedural-activity.git
    ```

## Important Link!
1. CUDA Compability
<a href="https://docs.nvidia.com/deploy/cuda-compatibility/index.html#cuda-intro">Here</a>
2. MM Detection Repository
<a href="https://github.com/open-mmlab/mmdetection">Here</a>
3. MM Pose Repository
<a href="https://github.com/open-mmlab/mmpose">Here</a>
4. MM Action2 Repository
<a href="https://github.com/open-mmlab/mmaction2">Here</a>
5. Steps for Completely removing CUDA Toolkit and NVIDIA Driver

    ```sh
    sudo apt-get --purge -y remove 'cuda*'
    sudo apt-get --purge -y remove 'nvidia*'
    sudo apt-get remove --purge '^nvidia-.*'
    sudo apt-get install ubuntu-desktop
    sudo rm /etc/X11/xorg.conf
    echo 'nouveau' | sudo tee -a /etc/modules
    sudo apt-get remove --purge '^nvidia-.*'
    sudo apt-get purge nvidia*
    sudo apt-get autoremove
    sudo apt-get autoclean
    sudo rm -rf /usr/local/cuda*
    ```

<!-- LICENSE -->
## License
This project is released under the [Apache 2.0 license](LICENSE).


[PyTorch]: https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white
[nVIDIA]: https://img.shields.io/badge/nVIDIA-%2376B900.svg?style=for-the-badge&logo=nVIDIA&logoColor=white
[Python]: https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54
[PyTorch-url]: https://pytorch.org/get-started/locally/
[nVIDIA-url]: https://www.nvidia.com/
[Python-url]: https://www.python.org