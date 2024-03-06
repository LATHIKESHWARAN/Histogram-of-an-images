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
```py
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("immg.jpeg")
color_image = cv2.imread("img.jpeg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Histogram of Grayscale image and color image
```py
import numpy as np
import cv2
Gray_image = cv2.imread("immg.jpeg")
Color_image = cv2.imread("img.jpeg")
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
```py

import cv2
gray_image = cv2.imread("immg.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/1693fc25-c984-43a9-9f4a-91a068653c92)






### Histogram of Grayscale Image and any channel of Color Image
### Grayscale image
![image](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/9e057e06-8622-4341-8adc-695d6cad2c52)


![image](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/bf9d87f9-0b7e-4209-b562-72b380f1e774)






### Color image

![Screenshot 2024-03-05 222450](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/4eacbe9d-62b2-4fd0-a69f-8be2e2ccc7c6)

![Screenshot 2024-03-05 222459](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/a8bc4dcc-0ec1-4b7f-9174-4165a572dfe4)

### Histogram Equalization of Grayscale Image.
![image](https://github.com/LATHIKESHWARAN/Histogram-of-an-images/assets/119393556/42a52c2c-9896-4c81-a6d7-a60917b1b045)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
