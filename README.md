# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.


### Step2:
Read the image and convert the bgr image to gray scale image.

### Step3:
Use any filters for smoothing the image to reduse the noise

### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:
Display the filtered image using plot and imshow

 
## Program:
```
DEVELOPED BY : jeevitha e
REG NO : 212222230054
```
# Import the packages
```
import cv2
import matplotlib.pyplot as plt
```
# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("f.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

# SOBEL EDGE DETECTOR
### SOBEL X AXIS :
```

sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### SOBEL X AXIS :
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```

# LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```


# CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()



```
## Output:
## SOBEL EDGE DETECTOR
### SOBEL X AXIS :
![image](https://github.com/Jeevithaelumalai/EDGEDETECTION/assets/118708245/3850a2cf-c684-4d11-a698-e7e2775ab889)


### SOBEL y AXIS :
![image](https://github.com/Jeevithaelumalai/EDGEDETECTION/assets/118708245/9a1ce7d7-0950-4589-9a97-3f44234abc7b)
### SOBEL XY AXIS:
![image](https://github.com/Jeevithaelumalai/EDGEDETECTION/assets/118708245/9edfb3a3-0384-4b05-b13b-84f6f1ea8989)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/Jeevithaelumalai/EDGEDETECTION/assets/118708245/98a613ed-a4a7-4d59-b0fb-d29b5a77a874)


### CANNY EDGE DETECTOR
![image](https://github.com/Jeevithaelumalai/EDGEDETECTION/assets/118708245/699d58bc-8256-40c8-be89-92cee69ddcd5)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
