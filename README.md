Problem Statment

In this project we build a vision based model for the shredder machine industry which is for the safety of human hand from the machine.rang the alarm while the hand is going the out of boreder of cirtain limit.

Discrption Overview :

We are hearing the number of cases that the people’s are loss their hands in machines for that we are come with an idea using the computer vision methods we can solve this problem . becase now a day the cctv is available every where and simply it can act like a 💂‍♀️ guard with using computer vision. We used SSD Lite as our model and MobileNet Weight
![1_GmJiirxTSuSVrh-r7gtJdA](https://user-images.githubusercontent.com/55822384/120699360-e7216f80-c4cd-11eb-94a9-66d310435007.png)


Here we are implemented this solution with higher accuracy with used ssd with used hike vision camera diffrent images of hand from a company which located in hosur.


![img1](https://user-images.githubusercontent.com/55822384/120697796-ca843800-c4cb-11eb-833c-5ef775544406.jpeg)


IMPLEMENTATION:

1 - detector_utils.py

From frozen_graph we can see the pre trained model 'ssd5_optimized_inference_graph.pb'.This is the actual model that is used for the object detection.
'/Glove_label_map.pbtxt' contain List of the strings that is used to add correct label for each box in here only the hand

here 2 classes are used:Hand, Closed Hand
Actual detection .. generate scores and bounding boxes given an image

it detect two hand at a time


2- orien_lines.py


Drawing the lines:
Machine Border line
Safety border line

3 - alert_check.py

 return the sound if the hand is going above the Safety border line
 
4 - hand_detection.py


it will open the frame there we can find out our two border that is Machine Border line and Safety border line . it will detect only two hands at a time 


<img width="786" alt="Screenshot 2021-05-19 at 10 47 59 AM" src="https://user-images.githubusercontent.com/55822384/118767243-1e233e80-b89b-11eb-9507-ace363658878.png">
