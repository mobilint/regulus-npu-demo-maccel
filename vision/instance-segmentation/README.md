# Instance Segmentation

Runs a YOLO segmentation model on a single image and overlays the per-instance
masks on top of the detection boxes; `yolov8n-seg.mxq` is included as a sample
model.

## How to build

Check the toolchain path inside `compile.sh` first, then build:

```bash
$ ./compile.sh
```

## How to run

```bash
$ cd build
$ ./inference ../yolov8n-seg.mxq ../../sample.jpg
$ ./inference_yaml ../yolov8n-seg.mxq ../../model_configs/yolov8n-seg.yaml ../../sample.jpg
```

`inference` uses the thresholds hard-coded in `inference.cc`, while
`inference_yaml` reads them from the YAML config; either way the annotated
image is written next to the input as `sample_result.jpg`. See
[../README.md](../README.md) for the YAML schema and the list of tested models.
