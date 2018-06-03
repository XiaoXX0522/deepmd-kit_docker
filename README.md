# Docker Engine Utility for DeePMD-kit
[DeePMD-kit](https://github.com/deepmodeling/deepmd-kit#run-md-with-native-code) is a deep learning package for many-body potential energy representation, optimization, and molecular dynamics.   
This docker project is set up to simplify the installation process of DeePMD-kit.
Thanks to @[TimChen314](https://github.com/TimChen314) and @[frankhan91](https://github.com/frankhan91) for the initial creation of this docker project.
For detailed usage please refer to the [paper](https://arxiv.org/abs/1712.03641) and [github repository](https://github.com/deepmodeling/deepmd-kit).

## Use docker images
For cpu only use `docker pull yixiaoc/deepmd:cpu`.
For gpu support use `docker pull yixiaoc/deepmd:gpu`.

## Build on your own
`git clone https://github.com/frankhan91/deepmd-kit_docker.git deepmd-kit_docker`   
`cd deepmd-kit_docker && docker build -f Dockerfile -t deepmd-kit_docker .`   
It will take a few minutes to download necessary package and install them.   
The `ENV` statement in Dockerfile sets the install prefix of packages. These environment variables can be set by users themselves.
The `ARG tensorflow_version` specifies the version of tensorflow to install, which can be set during the build command through `--build-arg tensorflow_version=1.5`.
