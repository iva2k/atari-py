# atari_py

[![Build Status](https://travis-ci.org/iva2k/atari-py.svg?branch=master)](https://travis-ci.org/iva2k/atari-py)
[![Build status](https://ci.appveyor.com/api/projects/status/eucf26971f5k9cli?svg=true)](https://ci.appveyor.com/project/iva2k/atari-py)

A Windows-MSYS2-MinGW compatible version of latest as of 2018-1112 from [https://github.com/openai/atari-py](https://github.com/openai/atari-py), which in turn is a packaged and slightly-modified version of [https://github.com/bbitmaster/ale_python_interface](https://github.com/bbitmaster/ale_python_interface).

Windows compatibility mods from [https://github.com/Kojoley/atari-py](https://github.com/Kojoley/atari-py).

This has been tested on Windows 7 (64-bit).  It will likely work on Windows XP or later.

## Installation

### First try Install OpenAI version

```pip install atari-py```

That *should* install a correct binary verison for your OS. If that does not work (e.g. on Windows) see next section.


### Install from Github Sources

If you have any `distutils` supported compiler you can install from sources:

```pip install git+https://github.com/iva2k/atari-py.git```


### Compiling and Installing from source

  -  make sure you have `git` and `cmake` system packages installed 
  -  clone the repo
  -  run `pip install -e .`

Alternatively, after cloning, you can install using `setuptools` by running:

```python setup.py install```


## Test Example

```python
import gym
env = gym.make('SpaceInvaders-v0')
env.reset()
for _ in range(1000):
    env.step(env.action_space.sample())
    env.render('human')
env.close()  # https://github.com/openai/gym/issues/893
```
