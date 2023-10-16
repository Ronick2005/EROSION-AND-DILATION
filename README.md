# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
### Step2:
Create the text image using cv2.putText.
### Step3:
Then create the structuring image for dilation/erosion.
### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.
### Step5:
Plot the images using plt.imshow.

## Program:
# Import the necessary packages
``` python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
``` python
text_image = np.zeros((100,600),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX 
cv2.putText(text_image,"Ronick Aakshath",(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Ronick's Output",text_image)
```
# Create the structuring element
``` python
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Erode the image
``` python
image_erode = cv2.erode(text_image,kernel)
cv2.imshow("Erode image",image_erode)
```
# Dilate the image
``` python
dilationImage=cv2.dilate(text_image,kernel)
cv2.imshow("Dilated Image",dilationImage)
```
## Output:

### Display the input Image
<br>
<br>
<br>
<br>
<br>
<br>

### Display the Eroded Image
<br>
<br>
<br>
<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>
<br>
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
