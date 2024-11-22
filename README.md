## Image_Acqusition-_using_Web_Camera
## Aim
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.

i) Write the frame as JPG

ii) Display the video

iii) Display the video by resizing the window

iv) Rotate and display the video

## Software Used
## Anaconda - Python 3.7

## Algorithm
## Step 1:
Use cv2.VideoCapture(0) to access web camera

## Step 2:
Use cv2.imread to read the video or image

## Step 3:
Use cv2.imwrite to save the image

## Step 4:
Use cv2.imshow to show the video

## Step 5:
End the program and close the output video window by pressing 'q'.

Program:
### Developed By:Bala murugan
### Register No:212222230017
## i) Write the frame as JPG file
```
import cv2
videoCaptureObject = cv2.VideoCapture(0)
ret, frame = videoCaptureObject.read()
if ret:
    cv2.imwrite("bala.jpg", frame)
videoCaptureObject.release()
cv2.destroyAllWindows()
```
## ii) Display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('bala',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

## iii) Display the video by resizing the window
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230017-bala',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230017-bala',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image


![WhatsApp Image 2024-11-09 at 11 32 45_da4edd45](https://github.com/user-attachments/assets/319bfe03-22ab-4ea5-ab59-8f928feb1ce9)

### ii) Display the video

![image](https://github.com/user-attachments/assets/8c263b4a-def0-460b-9561-137838b5a5d6)


### iii) Display the video by resizing the window
![image](https://github.com/user-attachments/assets/b344b446-332f-42c3-85ad-f04884d0a485)



### iv) Rotate and display the video

![image](https://github.com/user-attachments/assets/3b0ac623-afcc-47ee-98a9-fbb2e274c2d0)






## Result:
Thus the image is accessed from webcamera and displayed using openCV.
