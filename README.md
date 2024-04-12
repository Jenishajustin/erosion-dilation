# Implementation of Erosion and Dilation
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


``` python
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt

#to read the color image
input_image_path='anime.jpg'
color_image=cv2.imread(input_image_path)

#convert the color image to grayscale
gray_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)

#perform edge detection using Canny
edges=cv2.Canny(gray_image,100,200)

#define the kernel size for erosion and dilation
kernel_size=5
kernel=np.ones((kernel_size,kernel_size),np.uint8)

#perform erosion
erosion=cv2.erode(edges,kernel,iterations=1)

#perform dilation
dilation=cv2.dilate(edges,kernel,iterations=1)

#display all images
plt.figure(figsize=(15,10))

plt.subplot(2,3,1)
plt.imshow(cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')

plt.subplot(2,3,2)
plt.imshow(gray_image,cmap='gray')
plt.title('Black and White Image')
plt.axis('on')

plt.subplot(2,3,3)
plt.imshow(edges,cmap='gray')
plt.title('Edge Segmentation')
plt.axis('on')

plt.subplot(2,3,4)
plt.imshow(erosion,cmap='gray')
plt.title('Erosion')
plt.axis('on')

plt.subplot(2,3,5)
plt.imshow(dilation,cmap='gray')
plt.title('Dilation')
plt.axis('on')

plt.show()


```
## Output:

### Display the input Image
<br>
<img src="https://github.com/Jenishajustin/erosion-dilation/assets/119405070/f9fcb6ab-d718-4fa3-8651-98b49b6a4c13">

<br>

### Display the Eroded Image
<br>
<img src="https://github.com/Jenishajustin/erosion-dilation/assets/119405070/80452686-8086-4022-9ade-1cf103981947">

<br>

### Display the Dilated Image
<br>
<img src="https://github.com/Jenishajustin/erosion-dilation/assets/119405070/9886fb08-7f72-47fb-b742-7c546e11b8f4">
<br>

### Full Output
<br>
<img src="https://github.com/Jenishajustin/erosion-dilation/assets/119405070/04f575d4-473e-4a3d-b11b-4c82f84c5462">
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
