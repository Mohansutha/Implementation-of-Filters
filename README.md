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
![1](https://user-images.githubusercontent.com/94828335/171204451-df6f31ea-da8b-4ea1-9c0c-1f32dcb8caba.png)
![2](https://user-images.githubusercontent.com/94828335/171204516-ea45a0bc-a4db-4dc0-abc4-e348ae3ceaaa.png)

</br>
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter

![3](https://user-images.githubusercontent.com/94828335/171204650-aeed7a60-d78b-4174-b10b-999c1fff7b0e.png)
![4](https://user-images.githubusercontent.com/94828335/171204737-6fdf3235-d350-49f0-9bda-99ec36a3c36d.png)


</br>
</br>
</br>
</br>
</br>

iii) Using Gaussian Filter

![5](https://user-images.githubusercontent.com/94828335/171204818-a2ee7626-2c7e-42cc-8bb8-cc6810ba2325.png)
![6](https://user-images.githubusercontent.com/94828335/171204851-7bf8cbad-332e-4da9-a900-2ba54136159a.png)

</br>
</br>
</br>
</br>
</br>

iv) Using Median Filter
![7](https://user-images.githubusercontent.com/94828335/171204932-1373f5dc-bb16-4f80-9714-a01221d2351b.png)
![8](https://user-images.githubusercontent.com/94828335/171205050-697ef9e0-3a8d-482d-a655-af16d2fadca8.png)

</br>
</br>
</br>
</br>
</br>

### 2. Sharpening Filters

</br>

i) Using Laplacian Kernal
![9](https://user-images.githubusercontent.com/94828335/171205287-f49feb25-90cf-4f5d-a82e-342bfce708da.png)
![10](https://user-images.githubusercontent.com/94828335/171205360-5fbfab9a-a5c4-492b-996f-924c87d81312.png)


</br>
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
![11](https://user-images.githubusercontent.com/94828335/171205437-d12818a9-1bbb-4e89-af9b-b1b64e60616c.png)
![12](https://user-images.githubusercontent.com/94828335/171205499-d5caf650-f5b4-43b9-85c9-cc0163370e0d.png)

</br>
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
