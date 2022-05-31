# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1

Import the necessary modules
</br>
</br> 

### Step2

For performing smoothing operation on a image.
</br>
</br> 

Average filter

kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)

Weighted average filter

kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)

Gaussian Blur
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)

Median filter
median=cv2.medianBlur(image2,13)


### Step3

For performing sharpening on a image.

Laplacian Kernel
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)

Laplacian Operator

laplacian=cv2.Laplacian(image2,cv2.CV_64F)
</br>
</br> 

### Step4

Display all the images with their respective filters.
</br>
</br> 

### Step5
</br>
</br> 

## Program:
### Developed By   :S.Mohan Raj
### Register Number:212221230065
</br>
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("tae.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()




```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()





```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()





```

iv) Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()





```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
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
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()





```

## OUTPUT:
### 1. Smoothing Filter

</br>

i) Using Averaging Filter

![1](https://user-images.githubusercontent.com/94828335/171207974-4f31babb-3512-4ce6-bf7b-6bed13bbd682.jpg)


</br>
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter

![2](https://user-images.githubusercontent.com/94828335/171208319-8164978d-e99d-4949-a2e4-535886748342.jpg)



</br>
</br>
</br>
</br>
</br>

iii) Using Gaussian Filter

![3](https://user-images.githubusercontent.com/94828335/171208517-eb03868a-92f7-469f-b7b0-40e06344186d.jpg)


</br>
</br>
</br>
</br>
</br>

iv) Using Median Filter

![4](https://user-images.githubusercontent.com/94828335/171208643-aa0d0a55-0e7b-41f5-b2bf-f101ac7c937f.jpg)


</br>
</br>
</br>
</br>
</br>

### 2. Sharpening Filters

</br>

i) Using Laplacian Kernal
"C:\Users\Magesh\OneDrive\Documents\mohan\5.jpg"


</br>
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
![6](https://user-images.githubusercontent.com/94828335/171209002-8979690c-ac8f-453e-99c6-087d0acb4056.jpg)


</br>
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
