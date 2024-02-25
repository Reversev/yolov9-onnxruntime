# YOLOv9 ONNXRuntime (Python)

Performing Object Detection for YOLOv9 with ONNXRuntime

![ONNXRUNTIME YOLOv9 Object Detection](https://github.com/Reversev/yolov9-onnxruntime/blob/main/assets/horses.jpg)


## Installation

```shell
git clone https://github.com/danielsyahputra/yolov9-onnxruntime.git
cd yolov9-onnxruntime
pip install -r requirements.txt
```

```requirements.txt``` partly comes from [https://github.com/WongKinYiu/yolov9](https://github.com/WongKinYiu/yolov9).


### ONNX Runtime
Use Nvidia GPU:
```pip install onnxruntime-gpu```

Otherwise:
```pip install onnxruntime```


### Inference on Image with CPU/GPU

(1) CPU: need onnxruntime

```python
pip install onnxruntime
python main.py --source inference/images/horse.jpg --weights weights/yolov9-c.onnx --classes weights/coco_names.yaml --image
```

(2) GPU: need onnxruntime-gpu
```python
pip install onnxruntime-gpu
python main.py --source inference/images/horse.jpg --weights weights/yolov9-c.onnx --classes weights/coco_names.yaml --image --device cuda
```


### Inference on Video

(1) CPU: need onnxruntime
```
pip install onnxruntime
python main.py --source inference/video/demo.mp4 --weights weights/yolov9-c.onnx --classes data/coco_names.yaml --video
```

(2) GPU: need onnxruntime-gpu
```
pip install onnxruntime-gpu
python main.py --source inference/video/demo.mp4 --weights weights/yolov9-c.onnx --classes data/coco_names.yaml --video --device cuda
```

# References:
[1] [https://github.com/WongKinYiu/yolov9](https://github.com/WongKinYiu/yolov9)

[2] [https://github.com/danielsyahputra/yolov9-onnx/tree/master](https://github.com/danielsyahputra/yolov9-onnx/tree/master)

## License / 许可
[MIT License](LICENSE)
