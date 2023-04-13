# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import the required packages.

## Step2:
Read the image and convert into gray image.

## Step3:
Remove the noise of the image using gaussian operator.

## Step4:
Find the sobel edge,laplacian edge,canny edge using the built in modules available in opencv.

## Step5:
Plot the edged image using matplotlib.

 
## Program:
# Import the packages
```python
import cv2
import matplotlib.pyplot as plt
```

# Load the image, Convert to grayscale and remove noise
```python
img=cv2.imread("maple.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
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


# SOBEL EDGE DETECTOR
```python
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
```python
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
```python
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
### SOBEL EDGE DETECTOR
![Screenshot_20230412_024006](https://user-images.githubusercontent.com/118889143/231412346-451a3a2f-e2c9-4fb5-a45d-17538568253d.png)
![Screenshot_20230412_024038](https://user-images.githubusercontent.com/118889143/231412421-3edc563b-3425-48b7-8f5b-4de885105709.png)

### LAPLACIAN EDGE DETECTOR
![Screenshot_20230413_020309](https://user-images.githubusercontent.com/118889143/231702398-1d550de8-bd87-476e-ac76-f9d5cbca3bed.png)

### CANNY EDGE DETECTOR
![Uploading Screenshot_20230413_020342.png…]()
