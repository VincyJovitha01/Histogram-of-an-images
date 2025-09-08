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
# Developed By: VINCY JOVITHA V
# Register Number: 212223230242

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('img0.jpg')
color_image = cv2.imread('img1.jpg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()      


import numpy as np
gray_image=cv2.imread('img0.jpg')
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
color_image=cv2.imread('img1.jpg')
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
gray_image = cv2.imread("img0.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()







```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/3864064e-caaf-47bc-886d-9df6f212be08)
![image](https://github.com/user-attachments/assets/9c65afc2-4751-4b70-898b-f75bc48cb054)




### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/user-attachments/assets/8fd49cb9-d484-407b-bf8d-bf8c5baa52a1)
![image](https://github.com/user-attachments/assets/efaec669-33b1-494e-a0e3-e252bef1497f)





### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/4618cee1-8dcc-4d47-909d-cd4a3078f815)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
