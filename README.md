# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image
 
## Programand Output

NAME: Dharini PV
REG.NO: 212222240024

### Import the necessary packages
``` Python

import cv2
import matplotlib.pyplot as plt

# Create a blank image (100 pixels high and 400 pixels wide)
img = np.zeros((100, 400), dtype='uint8')
```

### Create the Text using cv2.putText
```python
# Put some text on the image for demonstration
cv2.putText(img, 'DhariniPV', (60, 70), cv2.FONT_HERSHEY_COMPLEX, 2, (255), 5)
```

### Create the structuring element
```python
# Create a rectangular structuring element
kernel_size = (5, 5)  # Width and height of the kernel
structuring_element = cv2.getStructuringElement(cv2.MORPH_RECT, kernel_size)

# Perform Erosion
eroded_image = cv2.erode(img, structuring_element, iterations=1)

# Perform Dilation
dilated_image = cv2.dilate(img, structuring_element, iterations=1)

# Display the original, eroded, and dilated images
plt.figure(figsize=(9, 3))
```
# Original Image
```python
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/f5e7ee0d-c3ef-4b1b-81d7-95a66d14a0ee)

# Erode the image
```python
plt.figure(figsize=(9, 3))
# Eroded Image
plt.imshow(eroded_image, cmap='gray')
plt.title('Eroded Image')
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/1c698744-a6ef-4fa2-a3e7-f9d3862edf12)

## Dilate the image
```python
plt.figure(figsize=(9, 3))
# Dilated Image
plt.imshow(dilated_image, cmap='gray')
plt.title('Dilated Image')
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/babf85ae-c3c4-4d44-b1a7-30ef3405a904)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
