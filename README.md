* How to run PyTorch with TinyGrad backend?
  *  Hints in [tinygrad test.yaml](https://github.com/tinygrad/tinygrad/blob/master/.github/workflows/test.yml). Sections: "Torch Backend Tests", "Torch Backend Tests More".
  *  Using miniconda for environment setup. [Install](https://www.anaconda.com/docs/getting-started/miniconda/install#linux).
  *  Setup:
    *  Install ninja-build
      * `sudo apt update` 
      * `sudo apt install -y ninja-build g++-11`
      * `sudo apt install -y llvm-15`
      * `export LLVM_CONFIG=/usr/bin/llvm-config-15`
    * Setup env
      * `conda create -n tinypytorch python=3.10`
      * `conda activate tinypytorch`
```sh
git clone https://github.com/tinygrad/tinygrad.git
cd tinygrad
python3 -m pip install -e .[testing_minimal]
conda install pytorch cudatoolkit=11.8 -c pytorch -c conda-forge
pip3 install --upgrade --force-reinstall ruff==0.11.0
pip3 install pillow torchvision expecttest
```

* Testing PytTorch with TinyGrad backend

     
        
