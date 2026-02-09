# Image_Acqusition-_using_Web_Camera
## Name: AJAYRAJA RATHINAM T
## Register no:212224240006

## Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Import OpenCV Package.

### Step 2:
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.

### Step 4:
Save Image to File. Employ 'imwrite' to save the captured image to a file.

### Step 5:
Display Video or Image. Use 'imshow' to display the captured video frame or image.

### Step 6:
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.


## Program:
### Developed By: AJAYRAJA RATHINAM T
### Register No: 212224240006


## i) Write the frame as JPG file

```PYTHON
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()
captured_image = cv2.imread('captured_frame.jpg')
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()

```


## ii) Display the video

```PYTHON
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```


## iii) Display the video by resizing the window

```PYTHON

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
  

```


## iv) Rotate and display the video

```PYTHON
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release() 
```

## Output

### i) Write the frame as JPG image
</br>
<img width="518" height="406" alt="Screenshot 2026-02-09 192535" src="https://github.com/user-attachments/assets/13c6fc92-2df3-41b9-a58e-b8dda0949728" />


</br>


### ii) Display the video
</br>
<img width="522" height="386" alt="Screenshot 2026-02-09 192640" src="https://github.com/user-attachments/assets/7dcfbda3-cc07-40c4-a744-8cb07113d93e" />


</br>


### iii) Display the video by resizing the window
</br>
<img width="257" height="381" alt="image" src="https://github.com/user-attachments/assets/a3875f1b-2c5d-4f2f-8df6-e94510e662b0" />


</br>



### iv) Rotate and display the video
</br>
<img width="296" height="382" alt="image" src="https://github.com/user-attachments/assets/c67359b7-000d-4ad9-a5da-1d5ecbdf3214" />


</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
