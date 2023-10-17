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
### Import the necessary packages
``` python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
``` python
text_image = np.zeros((100,550), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX 
cv2.putText(text_image, "Ronick Aakshath", (5,70), font, 2, (255), 5, cv2.LINE_AA)
plt.imshow(text_image)
```
### Create the structuring element
``` python
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS, (7,7))
```
### Erode the image
``` python
image_erode = cv2.erode(text_image, kernel)
plt.imshow(image_erode)
```
### Dilate the image
``` python
dilationImage=cv2.dilate(text_image, kernel)
plt.imshow(dilationImage)
```
## Output:
### Display the input Image
![image](https://github.com/Ronick2005/EROSION-AND-DILATION/assets/83219341/c32a65e6-1ec3-47a1-93d8-a1911f82840a)

### Display the Eroded Image
![image](https://github.com/Ronick2005/EROSION-AND-DILATION/assets/83219341/ba297106-951e-4820-a154-dbe9baeb1d4a)

### Display the Dilated Image
![image](https://github.com/Ronick2005/EROSION-AND-DILATION/assets/83219341/a96ebbfb-27db-4c46-96be-db5ef6c5b697)

## Result
Thus the generated text image is eroded and dilated using Python and OpenCV.
