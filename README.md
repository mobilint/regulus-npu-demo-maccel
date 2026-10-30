Sample program for Mobilint Regulus
===================================

Sample applications for the Mobilint Regulus NPU. Each directory is
self-contained and can be built on its own.

| Directory | What it does |
|---|---|
| [hello-world](hello-world) | Toolchain smoke test; does not touch the NPU |
| [image-classification-resnet50](image-classification-resnet50) | ResNet-50 on a single ImageNet image, in C++ and Python |
| [vision](vision) | Single-image samples for five vision tasks, with YAML-driven pre/post-processing |
| [face-detection-yolov8n](face-detection-yolov8n) | YOLOv8n face detection from a video file or a camera device |
| [1-usb-camera-3-models-hdmi-out](1-usb-camera-3-models-hdmi-out) | USB camera to three models to 1920x1080 HDMI output |

The samples under `vision` are built with CMake through `compile.sh`; every
other directory is built with `make`. See the README inside each directory for
build and run details.
