# Image Classification

Classifies a single image and writes the predicted label onto it;
`resnet18_torchvision.mxq` is included as a sample model and `imagenet.txt`
supplies the 1000 ImageNet class names. Unlike the other tasks this directory
only ships `inference_yaml`, because the preprocessing differs enough between
classification backbones that it is always taken from the YAML config.

## How to build

Check the toolchain path inside `compile.sh` first, then build:

```bash
$ ./compile.sh
```

## How to run

```bash
$ cd build
$ ./inference_yaml ../resnet18_torchvision.mxq ../../model_configs/resnet18.yaml ../../sample.jpg
```

The annotated image is written next to the input as `sample_result.jpg`. See
[../README.md](../README.md) for the YAML schema and the list of tested models.
