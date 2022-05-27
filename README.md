# Result
![image](https://user-images.githubusercontent.com/52165649/167928120-f2733f20-2b68-448e-99ab-7f2c1099dae2.png)
![image](https://user-images.githubusercontent.com/52165649/167928156-3f26c28c-0719-4a6a-8eb1-20fce2e12a32.png)
# установка зависимостей
pip install -r requirements.txt

# save yolov4-tiny model
python save_model.py --weights ./data/yolov4-tiny.weights --output ./checkpoints/yolov4-tiny-416 --model yolov4 --tiny

# Run yolov4-tiny object tracker
python object_tracker.py --weights ./checkpoints/yolov4-tiny-416 --video ./data/video/test.mp4 --output ./outputs/tiny.avi --tiny

python object_tracker.py --weights ./checkpoints/yolov4-tiny-416 --video 0 --output ./outputs/tiny.avi --tiny

# Run yolov4-tiny object tracker без сохранения видео
python object_tracker.py --weights ./checkpoints/yolov4-tiny-416 --video ./data/video/test.mp4 --tiny
