# Getting CascadeXML up and running


```bash
git clone https://github.com/xmc-aalto/cascadexml.git
cd cascadexml

# Conda setup
# python 3.11 is important, 3.12 is too new 
conda create --name xml-env python=3.11
conda activate xml-env

# base packages
conda install numpy
pip3 install torch
pip3 install scipy
pip3 install transformers
pip3 install scikit-learn

# dependencies for pyxclib
conda install Cython
pip install fasttext

# pyxclib 
git clone https://github.com/kunaldahiya/pyxclib.git
cd pyxclib
python3 setup.py install
# make sure that xclib is installed via `pip freeze -l | grep xclib`

# remaining dependencies
# llvmlite via conda, issues dependency warning, conflict with numba
# fix depedency warning by updating numba
cd ..  
pip install six
conda install llvmlite
pip install -U numba  
pip install nltk
```
