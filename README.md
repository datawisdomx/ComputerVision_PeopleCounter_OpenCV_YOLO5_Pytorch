# ComputerVision_PeopleCounter_OpenCV_YOLO5_Pytorch
Computer Vision model for livestream frame people counter. Using OpenCV, YOLO5  from ultralytics, pytorch
YOLO5 used the COCO image dataset for training its model 

Logic:
The OpenCV library used to get the livestream features cameras; the livestream is passed frame by frame to the YOLOv5 model for object detection. 
If the image contains a ‘person’, the people counter is updated. Total number of people in the image is printed at the end.

Results:
The model performs well in controlled environment, with close range images, proper lighting, etc. 100% accuracy. 
The algorithm was able to detect the correct number of people in the image, even if partly visible and contain other objects. 

The model performs poorly in an outside external environment. Accuracy drops below 50%
For the close range images, the correct number of people are detected.
For the long range images, the model does not detect people or objects in the image, which is a limitation of the camera quality (macbook air)
and YOLOv5 model library being used.
Model detects unique people when there is a major overlap of people in the frame. 
If people are beyond 20-25 meters or on higher floors, the model fails to detect people, as the cameras are located within the range and on the same floor 
as people we are trying to detect.

Summary:
Overall its a good model and easy to use with pytorch. 
Using better camera or other models like SSD can improve the overall accuracy

The code can be extended to perform object detection on a variety of object categories (80 in COCO) and use the livestream instead of just frames.


