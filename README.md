# YOLOv9 ONNXRuntime (Python)

Performing Object Detection for YOLOv9 with ONNXRuntime

![! ONNX YOLOv9 Object Detection](https://github.com/danielsyahputra/yolov9-onnx/blob/master/output/sample_image.jpeg)


## Installation

```shell
git clone https://github.com/danielsyahputra/yolov9-onnxruntime.git
cd yolov9-onnxruntime
pip install -r requirements.txt
```

```requirements.txt``` partly comes from [https://github.com/WongKinYiu/yolov9](https://github.com/WongKinYiu/yolov9).


### ONNX Runtime
For Nvidia GPU computers:
`pip install onnxruntime-gpu`

Otherwise:
`pip install onnxruntime`


### Inference on Image with CPU/GPU

(1) CPU: need onnxruntime

```python
pip install onnxruntime
python main.py --source assets/sample_image.jpeg --weights weights/yolov9-c.onnx --classes weights/metadata.yaml --image
```

(2) GPU: need onnxruntime-gpu
```python
pip install onnxruntime-gpu
python main.py --source assets/sample_image.jpeg --weights weights/yolov9-c.onnx --classes weights/metadata.yaml --image --device cuda
```


### Inference on Video

(1) CPU: need onnxruntime
```
pip install onnxruntime
python main.py --source assets/road.mp4 --weights weights/yolov9-c.onnx --classes weights/metadata.yaml --video
```

(2) GPU: need onnxruntime-gpu
```
pip install onnxruntime-gpu
python main.py --source assets/road.mp4 --weights weights/yolov9-c.onnx --classes weights/metadata.yaml --video --device cuda
```

# References:
[1] [https://github.com/WongKinYiu/yolov9](https://github.com/WongKinYiu/yolov9)

[2] [https://github.com/danielsyahputra/yolov9-onnx/tree/master](https://github.com/danielsyahputra/yolov9-onnx/tree/master)

## License / 许可
[MIT License](LICENSE)