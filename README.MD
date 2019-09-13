# Capstone Project

## Requirements

* Python 3.7
* Anaconda / Conda
* Preferrably some GPUs for the LSTM network training
* see imports in the start of the jupyter notebook for a list of the needed requirements
* install requirements from the "requirements.txt" file

One specific required library is "python-glove". However, this library is only compatible with python 2. Please follow the below instructions to port it to python 3 and install it:

```python

cd glove-python/glove

cython glove_cython.pyx
cythonize glove_cython.pyx

cython metrics/accuracy_cython.pyx
cythonize metrics/accuracy_cython.pyx

cython --cplus corpus_cython.pyx
cythonize corpus_cython.pyx

cd ..

python3 setup.py cythonize

pip install -e .

```
