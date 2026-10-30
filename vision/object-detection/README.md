# Object Detection

Runs a YOLO or SSD detector on a single image and draws the resulting boxes;
`yolov8n.mxq` is included as a sample model. `inference.cc` picks the
post-processor from the model filename, so anchor-based (`yolov5`, `yolov7`),
anchor-free (other `yolo`) and `ssd` models are all handled by the same binary.

## How to build

Check the toolchain path inside `compile.sh` first, then build:

```bash
$ ./compile.sh
```

## How to run

```bash
$ cd build
$ ./inference ../yolov8n.mxq ../../sample.jpg
$ ./inference_yaml ../yolov8n.mxq ../../model_configs/yolov8n.yaml ../../sample.jpg
```

`inference` uses the thresholds hard-coded in `inference.cc`, while
`inference_yaml` reads them from the YAML config; either way the annotated
image is written next to the input as `sample_result.jpg`. See
[../README.md](../README.md) for the YAML schema and the list of tested models.
