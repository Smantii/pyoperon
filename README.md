# pyoperon

[![License](https://img.shields.io/github/license/heal-research/pyoperon?style=flat)](https://github.com/heal-research/pyoperon/blob/master/LICENSE)
[![build-linux](https://github.com/heal-research/pyoperon/actions/workflows/build-linux.yml/badge.svg?branch=cpp20)](https://github.com/heal-research/pyoperon/actions/workflows/build-linux.yml)
[![Gitter chat](https://badges.gitter.im/operongp/gitter.png)](https://gitter.im/operongp/community)

**pyoperon** is the python bindings library of [**Operon**](https://github.com/heal-research/operon), a modern C++ framework for symbolic regression developed by [Heal-Research](https://github.com/heal-research) at the University of Applied Sciences Upper Austria.

A scikit-learn regressor is also available:
```python
from pyoperon.sklearn import SymbolicRegressor
```

The [examples](https://github.com/heal-research/pyoperon/examples) folder contains sample code for using either the Python bindings directly or the **pyoperon.sklearn** module.

# Installation

Due to ABI incompatiblity, the PyOperon version on PyPI is outdated. The wheels are instead released on github: https://github.com/heal-research/pyoperon/releases/

## Building from source

### Conda/Mamba

1. Clone the repo and switch to the `cpp20` branch
```
git clone https://github.com/heal-research/pyoperon.git
cd pyoperon
git switch cpp20
```

2. Install and activate the environment (replace micromamba with your actual program)
```
micromamba env create -f environment.yml
micromamba activate pyoperon
```

3. Install the dependencies
```
./scripts/dependencies.sh
```

4. Install `pyoperon`
```
pip install .
```

### Nix

Use this [environment](https://github.com/foolnotion/poetryenv) created with [poetry2nix](https://github.com/nix-community/poetry2nix)

```
nix develop github:foolnotion/poetryenv --no-write-lock-file
```

This will install operon and dependencies. Modify the flake file if you need additional python libraries (see https://github.com/nix-community/poetry2nix#how-to-guides)


# Contributing

See the [CONTRIBUTING](CONTRIBUTING.md) document.
