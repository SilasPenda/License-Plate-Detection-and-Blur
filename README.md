# License Plate Detection and Blurring Using Yolov4, Openvino

Clone this repo & cd into it

Download IR model and drop in folder

https://drive.google.com/drive/folders/1gxqqcMACrjvegS0_OQypeT_lDKarco5_?usp=sharing

Download video for inference and drop in folder

https://drive.google.com/file/d/1xxcud0qlQ4xcEgrjNntLGmNlxncuTZRU/view?usp=sharing

Create and activate Openvino Virtual environment.

```
python -m venv yolov4-openvino
.\yolov4-openvino\Scripts\activate
```

Install requirements

```
pip install -r requirements.txt
```

Run inference without blurring

```
python object_detection.py -m yolo-v4-tf.xml -at yolov4 --labels obj.names -i lp.mp4 -o output.mp4
```

Run inference with blurring

```
python object_detection.py -m yolo-v4-tf.xml -b -at yolov4 --labels obj.names -i lp.mp4 -o output.mp4
```
