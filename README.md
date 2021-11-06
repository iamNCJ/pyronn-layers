# pyronn-layers

This repo is intended for a CUDA 11 build for [PYRO-NN-LAYERS](https://github.com/csyben/PYRO-NN-Layers). It can also serve as a reference if you are suffering building custom ops following the outdated template provided by tensorflow official.

The most important fixes are picked from [Tensorflow Addons](https://github.com/tensorflow/addons), where they provided a newer CUDA detection script and other fixes.



## Build

Built on docker image [2.5.0-custom-op-ubuntu16](https://hub.docker.com/layers/tensorflow/tensorflow/2.5.0-custom-op-ubuntu16/images/sha256-f0676af86cb61665ae20c7935340b4073e325ccbad1f2bc7b904577dd6d511c0?context=explore), **not tested** on any other image.

```bash
./configure.sh
bazel build build_pip_pkg
bazel-bin/build_pip_pkg artifacts
```



## Install

Proofed working on [2.5.0-gpu](https://hub.docker.com/layers/tensorflow/tensorflow/2.5.0-gpu/images/sha256-0cb24474909c8ef0a3772c64a0fd1cf4e5ff2b806d39fd36abf716d6ea7eefb3?context=explore), **not tested** on any other image.

```bash
pip install pyronn_layers-0.1.4.2-cp36-cp36m-linux_x86_64.whl
pip install pyronn
```

Now it should work!
