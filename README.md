# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.

## Program:
### Developed By:POPURI SRAVANI
### Register Number:212223240117
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as 
image = cv2.imread('pcb.jpg', cv2.IMREAD_GRAYSCALE)
kernel = np.ones((4, 4), np.float32) / 9
averaged_image = cv2.filter2D(image, -1, kernel)
plt.imshow(averaged_image, cmap='gray')
plt.title("Averaging Filter")
plt.axis('off')
plt.show()

```
ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()

```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()

```
iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()

```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()

```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()

```

## OUTPUT:
### Original Image
![image](https://github.com/user-attachments/assets/38864be8-8276-4654-8335-26531b411e1b)

### 1. Smoothing Filters


i) Using Averaging Filter
![image](https://github.com/user-attachments/assets/66505e2d-81aa-41b0-88a2-e138059432be)

ii)Using Weighted Averaging Filter
![image](https://github.com/user-attachments/assets/d3cde3e3-2a8e-4ce4-a1b2-c92cbed2119e)


iii)Using Gaussian Filter
![image](https://github.com/user-attachments/assets/2ed61a43-b0d7-4bb3-adf0-1ebd6e717690)


iv) Using Median Filter
![image](https://github.com/user-attachments/assets/d2baa930-48b0-479e-9a72-d04c8eef669f)


### 2. Sharpening Filters

i) Using Laplacian Kernal
![image](https://github.com/user-attachments/assets/e6bd6bb7-17cf-4d3d-8766-ba9546ee8124)


ii) Using Laplacian Operator
![image](https://github.com/user-attachments/assets/92fdbac7-5c49-4a42-9eb4-0117cdc4a326)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
