## 1. Train/Detect/Test/Export
You can directly use these functions by importing them:
from yolov5 import train, val, detect, export
# from yolov5.classify import train, val, predict
# from yolov5.segment import train, val, predict

train.run(imgsz=640, data='coco128.yaml')
val.run(imgsz=640, data='coco128.yaml', weights='yolov5s.pt')
detect.run(imgsz=640)
export.run(imgsz=640, weights='yolov5s.pt')

-  You can pass any argument as input:
from yolov5 import detect

img_url = 'https://github.com/ultralytics/yolov5/raw/master/data/images/zidane.jpg'

detect.run(source=img_url, weights="yolov5s6.pt", conf_thres=0.25, imgsz=640)