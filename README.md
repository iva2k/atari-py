# atari_py

[![Build Status](https://travis-ci.org/openai/atari-py.svg?branch=master)](https://travis-ci.org/openai/atari-py)

A Windows-MSYS2-MinGW compatible version of [https://github.com/openai/atari-py](https://github.com/openai/atari-py), which in turn is a packaged and slightly-modified version of [https://github.com/bbitmaster/ale_python_interface](https://github.com/bbitmaster/ale_python_interface).

This has NOT YET been tested on Windows 7 (32 or 64-bit).  It will NOT YET likely work on Windows XP or later.

## Installation

To install via pip, run:

```pip install atari-py```
That *should* install a correct binary verison for your OS. If that does not work (or if you would like get the latest-latest
version, or you just want to tinker with the code yourself) see next paragraph. 

### Installation from source

  -  make sure you have `git`, `cmake` and `zlib1g` system packages installed 
  -  clone the repo
  -  run `pip install -e .`

### Alternatively, you can install using setuptools using:

```python setup.py install```

