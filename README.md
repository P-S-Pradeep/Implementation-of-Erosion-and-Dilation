# Implementation-of-Erosion-and-Dilation

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Erode the image using cv2.erode().

### Step5:
Dilate the image using cv2.dilate().

 
## Program:

```python

# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Load the Image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
# Create the Text using cv2.putText
cv2.putText(img1,'Pradeep',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
# Erode the image
img_erode=cv2.erode(img1,kernel1)
plt.imshow(img_erode,cmap='gray')

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
plt.imshow(img_dilate,cmap='gray')


```
## Output:

### Display the input Image
[1]![Screenshot (33)](https://user-images.githubusercontent.com/102652887/170830501-4c584b8d-9505-4764-a3b3-312e4241dc5b.png)


### Display the Eroded Image
[2]![Screenshot (34)](https://user-images.githubusercontent.com/102652887/170830510-1293cbc8-42c3-4f06-b207-9e6cf87d11f3.png)



### Display the Dilated Image
[3]![Screenshot (35)](https://user-images.githubusercontent.com/102652887/170830520-46310d45-21a9-421a-99da-047a57a8321c.png)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
