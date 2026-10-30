# Pose Estimation

Runs a YOLO pose model on a single image and draws the detected person boxes
together with their keypoint skeletons; `yolov8n-pose.mxq` is included as a
sample model.

## How to build

Check the toolchain path inside `compile.sh` first, then build:

```bash
$ ./compile.sh
```

## How to run

```bash
$ cd build
$ ./inference ../yolov8n-pose.mxq ../../sample.jpg
$ ./inference_yaml ../yolov8n-pose.mxq ../../model_configs/yolov8n-pose.yaml ../../sample.jpg
```

`inference` uses the thresholds hard-coded in `inference.cc`, while
`inference_yaml` reads them from the YAML config; either way the annotated
image is written next to the input as `sample_result.jpg`. See
[../README.md](../README.md) for the YAML schema and the list of tested models.
