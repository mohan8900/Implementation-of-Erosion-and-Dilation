# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>Import the necessary packages.


### Step2:
<br>
Create the text image.

### Step3:
<br>Create the structuring image for dilation/erosion.

### Step4:
<br>

Apply erosion and dilation using cv2.erode and cv2.dilate.
### Step5:
<br>
Display the images.

 
## Program:

``` Python
# Import the necessary packages

Developed by : MOHANRAJ A K

Register Number : 212221230064

import numpy as np 
import cv2
import matplotlib.pyplot as plt



# Create the Text using cv2.putText

img1=np.zeros((100,200),dtype= 'uint8') 
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,' VICKY',(7,70),font,1.4,(255),7,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
plt.title("Original Image")
plt.axis('OFF')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))



# Erode the image

image_erode = cv2.erode(img1,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,cmap='gray')
plt.axis('off')


# Dilate the image
image_dilate = cv2.dilate(img1,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,cmap='gray')
plt.axis('off')




```
## Output:

### Display the input Image
![output](.//VI3.png)

### Display the Eroded Image
![output](.//VI2.png)

### Display the Dilated Image
![output](.//VI1.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
