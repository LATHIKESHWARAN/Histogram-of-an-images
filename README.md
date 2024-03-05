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

### Developed By: LATHIKESHWARAN J
### Register Number: 212222230072

### Grayscale image and Color image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gray.jpeg")
color_image = cv2.imread("dip.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Histogram of Grayscale image 
```
import numpy as np
import cv2
Gray_image = cv2.imread("gray.jpeg")
Color_image = cv2.imread("dip.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
### Histogram of Color image
```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
### Histogram equalization of Grayscale image
```

import cv2
gray_image = cv2.imread("dip.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-05 222035](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/40e1b43f-c9c1-4e59-b5f5-8d1aacf42403)

![Screenshot 2024-03-05 222053](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/0f75d66a-fae8-4e21-9615-e6e4d5c53536)





### Histogram of Grayscale Image and any channel of Color Image
### Grayscale image
![Screenshot 2024-03-05 222355](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/9523ef5a-5de6-4f63-9261-524738b20392)

![Screenshot 2024-03-05 222414](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/8737af8c-b435-4c09-aa26-05663f696e2a)





### Color image

![Screenshot 2024-03-05 222450](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/4eacbe9d-62b2-4fd0-a69f-8be2e2ccc7c6)

![Screenshot 2024-03-05 222459](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/a8bc4dcc-0ec1-4b7f-9174-4165a572dfe4)

### Histogram Equalization of Grayscale Image.
![image](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/6d7cc627-2489-43c0-b0de-709fb44a391d)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
