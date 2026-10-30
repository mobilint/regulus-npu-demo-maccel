# image-classification-resnet50

ResNet-50 classification of a single ImageNet validation image, provided twice:
`resnet50.cc` on the C++ runtime and `resnet50.py` on the Python binding.
Both preprocess the image the same way (resize to 256, center-crop to 224,
normalize with the torchvision mean/std) and print the expected label next to
the predicted one.

## How to build

    make

## How to run

The model path and the input image are hard-coded, so run the binary from this
directory:

    ./resnet50

The Python version takes an optional `.mxq` path:

    python3 resnet50.py [resnet50.mxq]
