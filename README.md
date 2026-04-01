OpenSfM
=======
[![Conda](https://github.com/mapillary/OpenSfM/actions/workflows/conda.yml/badge.svg)](https://github.com/mapillary/OpenSfM/actions/workflows/conda.yml) [![Docker Ubuntu 20.04](https://github.com/mapillary/OpenSfM/actions/workflows/docker_ubuntu20.yml/badge.svg)](https://github.com/mapillary/OpenSfM/actions/workflows/docker_ubuntu20.yml) [![Docker Ubuntu 24.04](https://github.com/mapillary/OpenSfM/actions/workflows/docker_ubuntu24.yml/badge.svg)](https://github.com/mapillary/OpenSfM/actions/workflows/docker_ubuntu24.yml)

## Setup on WSL 2

- Distribution: Ubuntu 24.04

### Install Dependencies

```
sudo apt update && sudo apt install -y build-essential cmake git libeigen3-dev libopencv-dev libceres-dev python3-dev python3-pip
```

### Install Miniconda
```
bash <(curl -s https://repo.anaconda.com/miniconda/Miniconda3-py312_26.1.1-1-Linux-x86_64.sh)
```

### Setup OpenSfM

```
git clone https://github.com/lwndhrst/OpenSfM.git --recursive
```

```
cd OpenSfM
```

```
conda env create -f conda.yml
```

```
conda activate opensfm
```

```
pip install --no-cache-dir -e .[test]
```

### Usage

```
bin/opensfm <command> <dataset_dir>
```

```
bin/opensfm_run_all <dataset_dir>
```



## Overview
OpenSfM is a Structure from Motion library written in Python. The library serves as a processing pipeline for reconstructing camera poses and 3D scenes from multiple images. It consists of basic modules for Structure from Motion (feature detection/matching, minimal solvers) with a focus on building a robust and scalable reconstruction pipeline. It also integrates external sensor (e.g. GPS, accelerometer) measurements for geographical alignment and robustness. A JavaScript viewer is provided to preview the models and debug the pipeline.

<p align="center">
  <img src="https://opensfm.org/docs/_images/berlin_viewer.jpg" />
</p>

Checkout this [blog post with more demos](http://blog.mapillary.com/update/2014/12/15/sfm-preview.html)


## Getting Started

* [Building the library][]
* [Running a reconstruction][]
* [Documentation][]


[Building the library]: https://opensfm.org/docs/building.html (OpenSfM building instructions)
[Running a reconstruction]: https://opensfm.org/docs/using.html (OpenSfM usage)
[Documentation]: https://opensfm.org/docs/ (OpenSfM documentation)

## License
OpenSfM is BSD-style licensed, as found in the LICENSE file.  See also the Facebook Open Source [Terms of Use][] and [Privacy Policy][]

[Terms of Use]: https://opensource.facebook.com/legal/terms (Facebook Open Source - Terms of Use)
[Privacy Policy]: https://opensource.facebook.com/legal/privacy (Facebook Open Source - Privacy Policy)
