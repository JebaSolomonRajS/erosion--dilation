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
 
## Program:
### Developed by: Jeba Solomon Raj S
### Register number: 212223230089
## PROGRAM
```
import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,700),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'Jeba Solomon' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')
```



## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/5bcb01c1-5672-4cad-87a9-8ef1ade271b6)


### Display the Eroded Image
![image](https://github.com/user-attachments/assets/633b9ec2-81aa-4cec-b1db-6ea2f0564a1c)


### Display the Dilated Image
![image](https://github.com/user-attachments/assets/8bf8ba32-680d-4ac5-ba48-dd154a1da91b)





## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

