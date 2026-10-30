# Face Detection

Runs a YOLO face model on a single image and draws the face boxes with their
five facial landmarks; `yolov8n-face.mxq` is included as a sample model.

## How to build

Check the toolchain path inside `compile.sh` first, then build:

```bash
$ ./compile.sh
```

## How to run

```bash
$ cd build
$ ./inference ../yolov8n-face.mxq ../../sample.jpg
$ ./inference_yaml ../yolov8n-face.mxq ../../model_configs/yolov8n-face.yaml ../../sample.jpg
```

`inference` uses the thresholds hard-coded in `inference.cc`, while
`inference_yaml` reads them from the YAML config; either way the annotated
image is written next to the input as `sample_result.jpg`. See
[../README.md](../README.md) for the YAML schema and the list of tested models.
