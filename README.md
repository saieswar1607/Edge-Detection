# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import all the required packages.
<br>


### Step2:

Load the image to operate on.
<br>

### Step3:

Convert the image to grayscale image.
<br>

### Step4:

Use Sobel operator along x,y and xy directions.
<br>

### Step5:

Operate the image using Laplacian operator.
<br>

### Step6:

Operate the image using Canny Edge operator.
<br>

### Step7:

Show all the operated images output.
<br>

 
## Program:

``` Python

import cv2
import matplotlib.pyplot as plt
image = cv2.imread("car.jpg")
cv2.imshow("Original Image",image)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)

## SOBEL EDGE DETETCTOR:
### SOBEL X:

sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'RdPu')
plt.title('RdPu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()

### SOBEL Y:

sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()

### SOBEL XY:

sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'BuPu')
plt.title('BuPu')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'BuPu')
plt.title('Sobel XY')
plt.xticks([])
plt.yticks([])
plt.show()


## LAPLACIAN EDGE DETECTOR:

laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()


## CANNY EDGE DETECTOR:

canny_edge = cv2.Canny(new_image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'gist_gray')
plt.title('gist_gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gist_gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR

Sobel X:
<br>
<img width="564" alt="1" src="https://user-images.githubusercontent.com/93427011/168776614-eecbbc8e-43ab-4b08-aa9d-1810507883cd.png">
<br>
Sobel Y:
<br>
<img width="564" alt="2" src="https://user-images.githubusercontent.com/93427011/168776692-a739ffbe-b80d-4bc6-8207-a0f1a7043366.png">
<br>
Sobel XY:
<br>
<img width="564" alt="3" src="https://user-images.githubusercontent.com/93427011/168776791-d1c6bea3-5fe0-4fc1-829a-8dbdbcd3b4fa.png">
<br>


### LAPLACIAN EDGE DETECTOR
<br>
<img width="564" alt="4" src="https://user-images.githubusercontent.com/93427011/168776852-1e0e6055-cdc9-46c2-b6e8-2ad6fee564ba.png">
<br>

### CANNY EDGE DETECTOR
<br>
<img width="564" alt="5" src="https://user-images.githubusercontent.com/93427011/168776898-7aac5cad-3f5a-4550-99ff-d1aee572ed9d.png">
<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
