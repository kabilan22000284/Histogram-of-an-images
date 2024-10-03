# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().
### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: Kabilan V
# Register Number: 2122222100018
pip install opencv-python

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('lm10.png')
color_image = cv2.imread('goat.jpg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import numpy as np
gray_image=cv2.imread('lm10.png')
import matplotlib.pyplot as plt 
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()

import numpy as np
color_image=cv2.imread('goat.jpg')
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()

import cv2
gray_image = cv2.imread("lm10.png",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image

![Screenshot 2024-09-19 113057](https://github.com/user-attachments/assets/13a077c9-868c-41c5-9c5d-ba4151c2a52f)
### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/user-attachments/assets/abad8c2c-9128-4286-877d-a9454528a8b8)

![image](https://github.com/user-attachments/assets/af98b0d9-a1d7-4d65-a247-30b25f19bfdf)

![image](https://github.com/user-attachments/assets/f1a38d39-3a36-40f5-948d-9ce4ccb55fdb)

![image](https://github.com/user-attachments/assets/a5f39ece-3d35-46a9-a176-e5c44bc89008)
### Histogram Equalization of Grayscale Image.

![image](https://github.com/user-attachments/assets/45f7cca3-efc7-4ce2-a299-6c076ad829b2)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
