# Record-THRESHOLDING
## Experiment No: 8
## Name:
Dharanya N
## Register Number:
212223230044

### Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

### Software Required
Anaconda - Python 3.7
OpenCV

### Algorithm
### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

### PROGRAM:
### Load the Packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


### Read the image and convert to grayscale
```
image = cv2.imread('Qn8_thresholding.tif')  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  # Convert to grayscale
```


### Display original Image
```python
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')
```


### Use Global Thresholding to segment the image
```python
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
```


### Use Adaptive Thresholding to segment the image
```python
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
```


### Use Otsu's method to segment the image
```python
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```


### Global Thresholding
```python
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```


### Adaptive Thresholding
```python
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```


### Otsu's Method
```python
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```


### Show the plot
```python
plt.tight_layout()
plt.show()
```

### Output:
i)Original image


<img width="209" height="210" alt="download" src="https://github.com/user-attachments/assets/b157d579-30ca-4032-b466-cbf087740d8b" />

ii)Global Thresholding


<img width="209" height="210" alt="download" src="https://github.com/user-attachments/assets/84c34425-4405-4c31-8720-05cd5abe00cf" />

iii) Adaptive Thresholding


<img width="209" height="210" alt="download" src="https://github.com/user-attachments/assets/6bae07a0-e524-4b10-92a7-ceb09f2252d2" />

iv)Otsu's Method


<img width="209" height="210" alt="download" src="https://github.com/user-attachments/assets/3efdb481-2a6f-4681-b6b7-c75db7f205ed" />

### Result:
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
