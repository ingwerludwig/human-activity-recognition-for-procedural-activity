<!-- ABOUT THE PROJECT -->
## About The Human Activity Recognition Project using Pytorch Framework
### Built With
* [![PyTorch][PyTorch]][PyTorch-url]
* [![Python][Python]][Python-url]
* [![nVIDIA][nVIDIA]][nVIDIA-url]


### Prerequisite
1. Python 3.12 Installed </br>
2. Conda Installed </br>

### Installation
_This is the installation guide for Setting Pytorch with CUDA GPU Support_

1. Install the NVIDIA GPU Driver 530.30.02 (It's must to use the exact driver version to support NVIDIA Toolkit 12.1)

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
2. Check the Installed GPU Driver Version
   ```sh
   nvidia-smi
   ```
3. Reboot the computer </br>
4. Install the CUDA Toolkit 12.1 (match with NVIDIA GPU Driver version) from NVIDIA Downloads Page preferred or Conda
Link NVIDIA Driver Downloads Page <a href="https://developer.nvidia.com/cuda-12-1-0-download-archive?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=20.04">here</a></br>
5. Install cuDNN match with the CUDA Toolkit and and NVIDIA GPU Driver
    ```sh
    conda install -c nvidia cuda-nvcc==12.1
    ```
   or
    ```sh
    conda install -c "nvidia/label/cuda-12.1.0" cuda-nvcc
    ```
6. Install Pytorch
    ```sh
    conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia
    ```
7. Verify GPU Support
    ```sh
    import torch
    print(torch.cuda.is_available())
    ```
8. Clone this project repository
    ```sh
    git clone https://github.com/ingwerludwig/human-activity-recognition-for-procedural-activity.git
    ```
9. Install all the package requirement
    ```sh
    pip install -r requirements.txt
    ```

<!-- LICENSE -->
## License
Distributed under the MIT License. See `LICENSE.txt` for more information.


[PyTorch]: https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white
[nVIDIA]: https://img.shields.io/badge/nVIDIA-%2376B900.svg?style=for-the-badge&logo=nVIDIA&logoColor=white
[Python]: https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54
[PyTorch-url]: https://pytorch.org/get-started/locally/
[nVIDIA-url]: https://www.nvidia.com/
[Python-url]: https://www.python.org