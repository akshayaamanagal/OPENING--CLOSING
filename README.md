# OPENING--CLOSING
# Aim
To implement Opening and Closing using Python and OpenCV.

# Software Required
1. Anaconda - Python 3.7
2. OpenCV
# Algorithm:
## Step1:
Import the necessary packages.
## Step2:

Create the Text using cv2.putText.
## Step3:

Create the structuring element.
## Step4:

Use Opening operation
## Step5:
Use Closing Operation 
# Program:
## DEVELOPED BY: AKSHAYAA M
## REGISTER NUMBER: 212222230009
``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(img1,'AKSHAYAA',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Use Opening operation
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel1)
plt.imshow(image1,cmap='gray')
plt.title('OPENING'), plt.xticks([]), plt.yticks([])
plt.show()

# Use Closing Operation
image1=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
plt.imshow(image1,cmap='gray')
plt.title('CLOSING'), plt.xticks([]), plt.yticks([])
plt.show()

```
# Output:

## Display the input Image
![OPENING--CLOSING](1.png)
## Display the result of Opening
![OPENING--CLOSING](2.png)
## Display the result of Closing
![OPENING--CLOSING](3.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
