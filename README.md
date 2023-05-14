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

Create the text image using cv2.putText.
### Step3:

Then create the structuring image for dilation/erosion.
### Step4:

Apply erosion and dilation using cv2.erode and cv2.dilate.
### Step5:

Plot the images using plt.imshow.

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create the Text using cv2.putText
text_image = np.zeros((100,550),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"LOGESHWARI.P",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')
# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
# Erode the image
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')
# Dilate the image
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')
```
## Output:

### Display the input Image

![DIP10A](https://github.com/logeshwari2004/Implementation-of-Erosion-and-Dilation/assets/94211349/366049f9-4592-4926-81b9-5aca3d46c42a)

### Display the Eroded Image
![DIP10B](https://github.com/logeshwari2004/Implementation-of-Erosion-and-Dilation/assets/94211349/b059dd3c-d1a6-440b-876f-dd65dfccafb9)

### Display the Dilated Image
![DIP10C](https://github.com/logeshwari2004/Implementation-of-Erosion-and-Dilation/assets/94211349/fb4ad9f5-7f8f-4771-9425-ca9b16354b7f)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
