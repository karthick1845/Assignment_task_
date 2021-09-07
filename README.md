# "Write a program to count the number of instances for each object class in the given traffic video clip. The count should be with respect to entire video and not with respect to single frame"

 To create an object tracking using Deep sort[Simple Online and Realtime Tracking with a Deep Association Metric] for tracking an each object in given output.
 
 * To detect an object using yolov4
 * Then it convert into Tensorflow.Because , I use Deep sort using tensorflow.
 * After using deep sort,to find our tracking results.
 
 # Use cases:
 
 * In this project, I mainly focussed on vehicle tracking(any other objects in coco dataset can be tracking ).
 * By this project you can use traffic surveillance cameras for how many vehicles are passing in busy time and try to reduced traffic system.
 * Its also used for large and small scale factories to count our production things much easy.
 * With help of tracking, we should handle so much daily regular task like : number plate recognition,traffic control system and many things.


# Test video demo : https://github.com/karthick1845/Assignment_task_/tree/main/data/video


# Result of demo : https://drive.google.com/drive/folders/1eIED4hOpm7EaoNW1PGIt8uaXM0GSEr2P?usp=sharing


 # Steps for your IDE
 
  1) Set a environment path with python==3.7

  2) download requirements.txt
       * For CPU --> pip install -r requirements.txt

       * For GPU --> pip install -r requirements-gpu.txt

  3) Download a yolo_v4 pretrained model:  https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v4_pre/yolov4-tiny.weights

  4) Put it into "data" folder

  5) Check a name of weight name :yolov4.weights

  Type in command prompt :

  6) Convert darknet weights into tensorflow model:
  python save_model.py --model yolov4

  7) Run yolov4 deep sort object tracker on video:

  python object_tracker.py --video ./data/video/Highway.mp4 --output ./outputs/demo1.avi --model yolov4

  [put your test video and saving name of output video]
  
 # GOOGLE COLAB
 
 Go to my colab notebook and copy it into your drive : https://colab.research.google.com/drive/1v7NedREfZIFvK9TtlH953ZwV77kuBWUW
 
 # Steps to run it on google colab [Already in my drive notebook]
 
  *  Set GPU as runtime

  *  Clone it : !git clone https://github.com/karthick1845/Assignment_task_.git.

  * Set path : %cd Assignment_task_/

  * Install reqirements : !pip install -r requirements-gpu.txt

  * If sometimes tensorflow version not working on some time :
               --> !pip uninstall tensorflow -y
               --> !pip install tensorflow==2.3.0

  * Download yolov4 and save it into "data" folder : !wget https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights -P data/

  * Convert yolov4 Darknet into Tensorflow model: !python save_model.py --model yolov4

  * Run an your tesy video :!python object_tracker.py --video ./data/video/Highway.mp4 --output ./outputs/custom.avi --model yolov4 --dont_show

  * Unfortunately colab not support display video format, so we convert into base64 model

  * Join it into our path in drive and show it.
