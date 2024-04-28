# EX 09 : Implementation of Erosion and Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
### Step2:
Read and convert the color image into grayscale image.

### Step3:
Perform edge detection using Canny.

### Step4:
Perform dilation and erosion.

### Step5:
Dislay the images.

 
## Program:
```
Developed By : J.JENISHA
Reg. No. : 212222230056
```

``` python
# Import the necessary packages :

import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText :

img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'JENISHA',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')

# Create the structuring element :

kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)

# Erode the image :

img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

# Dilate the image :

img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
<br>
<img src="https://github.com/Jenishajustin/erosion-dilation/assets/119405070/3b155592-6f65-4f43-9661-4f90f6defe2b">

<br>

### Display the Eroded Image
<br>
<img src="https://github.com/Jenishajustin/erosion-dilation/assets/119405070/413caf35-e1c4-4bf4-b250-4ba3de23a562">

<br>

### Display the Dilated Image
<br>
<img src="https://github.com/Jenishajustin/erosion-dilation/assets/119405070/005bdb73-3b65-41f2-bf1f-ec9ac53dff11">

<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
