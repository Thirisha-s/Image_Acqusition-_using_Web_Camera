[# Image-Acquisition-from-Web-Cameraa
## Aim

To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera
<br>

### Step 2:
Use cv2.imread to read the video or image
<br>

### Step 3:
Use cv2.imwrite to save the image
<br>

### Step 4:
Use cv2.imshow to show the video
<br>

### Step 5:
End the program and close the output video window by pressing 'q'.
<br>

## Program:
#### Developed By: TIRISHA.S
#### Register No: 212222230160
```python
# i) Write the frame as JPG file

import cv2
videoCaptureObject = cv2.VideoCapture(0)
while (True):
    ret,frame = videoCaptureObject.read()
    cv2.imwrite("trial.jpeg",frame)
    result = False
videoCaptureObject.release()
cv2.destroyAllWindows()
```


```python
# ii) Display the video
import cv2
videoCaptureObject = cv2.VideoCapture(0)
while(True):
    ret,frame = videoCaptureObject.read()
    cv2.imshow('myimage',frame)
    if cv2.waitKey(1) == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()
```

```python
# iii) Display the video by resizing the window
import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read() 
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8) 
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5) 
    image[:height//2, :width//2] = smaller_frame
    image[height//2:, :width//2] = smaller_frame
    image[:height//2, width//2:] = smaller_frame 
    image [height//2:, width//2:] = smaller_frame
    cv2.imshow('myimage', image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```


```python
# iv) Rotate and display the video
import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read() 
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8) 
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5) 
    image[:height//2, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[:height//2, width//2:] = smaller_frame 
    image [height//2:, width//2:] = smaller_frame
    cv2.imshow('myimage', image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image
![2](https://github.com/Yogeshvar005/Image_Acqusition-_using_Web_Camera/assets/113497367/b188bcef-3ff3-4135-947b-ea07117b2a79)                                 
![image](https://github.com/Yogeshvar005/Image_Acqusition-_using_Web_Camera/assets/120380280/27a24144-4b49-4279-96f2-b9a2a2378b0f)


</br>
</br>


### ii) Display the video
![4](https://github.com/Yogeshvar005/Image_Acqusition-_using_Web_Camera/assets/113497367/739d3d28-d1bc-43eb-88c8-44f5a54e4495)      
![image](https://github.com/Yogeshvar005/Image_Acqusition-_using_Web_Camera/assets/120380280/64a16dd8-fe0d-4eb7-b07b-0faeedb7368d)



</br>
</br>


### iii) Display the video by resizing the window
![6](https://github.com/Yogeshvar005/Image_Acqusition-_using_Web_Camera/assets/113497367/e6219f79-5c75-4776-aad8-e41a336dfb3e)     
![image](https://github.com/Yogeshvar005/Image_Acqusition-_using_Web_Camera/assets/120380280/f9d6522b-ca0b-452c-b3a3-eddad4b7ecc2)


</br>
</br>



### iv) Rotate and display the video
![8](https://github.com/Yogeshvar005/Image_Acqusition-_using_Web_Camera/assets/113497367/faf660f3-a8fc-467e-9aad-d779963ade0e)    
![image](https://github.com/Yogeshvar005/Image_Acqusition-_using_Web_Camera/assets/120380280/78f66873-2b32-464b-9dd9-afc4f42fe381)


</br>
</br>


## Result 
Thus the image is accessed from webcamera and displayed using openCV.
](https://github.com/Augustine0306/Image_Acqusition-_using_Web_Camera.git)https://github.com/Augustine0306/Image_Acqusition-_using_Web_Camera.git
