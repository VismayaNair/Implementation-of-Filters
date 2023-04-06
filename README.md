# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1 : Import the required packages .
</br>
</br> 

### Step2 : Use the methods for performing smoothening on the given image one by one and display them.
</br>
</br> 

### Step3
</br> Perform sharpening on the given image using the Laplacian methods
</br> 

### Step4
</br> Display the sharpened image using the required functions
</br> 

### Step5
</br> End the execution 
</br> 

## Program:
### Developed By   : VISMAYA.S
### Register Number: 212221230125
</br>

# READING THE IMAGE :

```Python 
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('d6.jpeg')
image2 = cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

kernel = np.ones((11,11),np.float32)/121
image3 = cv2.filter2D(image2,-1,kernel)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("212221230125")
plt.axis('off')
plt.show()
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('average')
plt.axis('off')
plt.show()


```
ii) Using Weighted Averaging Filter
```Python

kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("212221230125")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average")
plt.axis("off")
plt.show()




```
iii) Using Gaussian Filter
```Python

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("212221230125")
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
plt.title("212221230125")
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
plt.title("212221230125")
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
plt.title("212221230125")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()



```

## OUTPUT:

### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>![1](https://user-images.githubusercontent.com/93427210/230450814-7e93c0a0-8c52-4d03-a48b-d44d90358338.png)
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter
</br>![2](https://user-images.githubusercontent.com/93427210/230450835-4fa32f4e-08c6-4b15-bc7c-446bd478f300.png)
</br>
</br>
</br>
</br>

iii) Using Gaussian Filter
</br>![3](https://user-images.githubusercontent.com/93427210/230450894-4a57ba47-b051-4340-9be0-9bd4bdc8f178.png)
</br>
</br>
</br>
</br>

iv) Using Median Filter
</br>![4](https://user-images.githubusercontent.com/93427210/230450942-d05d7a98-a611-4430-91d5-a2b02957bb69.png)
</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>![5](https://user-images.githubusercontent.com/93427210/230450980-69feb28d-eb90-47f4-8d43-2d7c41b23414.png)
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
</br>![6](https://user-images.githubusercontent.com/93427210/230451008-346f462c-37fb-46ed-b68d-b6feb879eafc.png)
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
