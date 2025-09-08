# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7




## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br>

Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 

## Program:
### Developed By : NITHISHKUMAR S
### Register Number: 212223240109
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("nature.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
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
plt.title("Median Blur")
plt.axis('off')
plt.show()

```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
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
### 1. Smoothing Filters
</br>

### i) Using Averaging Filter
<img width="687" height="437" alt="image" src="https://github.com/user-attachments/assets/124ef18e-8082-46a8-8dcd-523d4b320a51" />

### ii)Using Weighted Averaging Filter
<img width="283" height="387" alt="image" src="https://github.com/user-attachments/assets/b570f496-b056-4ad7-9bcf-ee3ec07f26e0" />



### iii)Using Gaussian Filter
<img width="292" height="381" alt="image" src="https://github.com/user-attachments/assets/12c2c992-e009-4fb9-a58c-03320e83fc30" />


### iv) Using Median Filter
<img width="408" height="386" alt="image" src="https://github.com/user-attachments/assets/c8ff72fa-98c1-4ee2-acc4-ae6b7444cc91" />


### 2. Sharpening Filters
</br>

### i) Using Laplacian Kernal
<img width="281" height="378" alt="image" src="https://github.com/user-attachments/assets/c0ad7cf8-4331-41c4-8cbe-2cece0b520e9" />


### ii) Using Laplacian Operator
<img width="267" height="370" alt="image" src="https://github.com/user-attachments/assets/ba630ab4-9f96-46d9-a934-b9ff56cfc831" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
