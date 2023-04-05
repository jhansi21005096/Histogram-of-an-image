# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the libraries.



### Step2:

Use cv2.calcHist to find the histogram of the image.
### Step3:
Plot the image and its stem plots using the functions.

### Step4:
Equalize the grayscale image using the in-built function cv2.equalizeHist().

### Step5:
Display the original and equalized image.

## Program:
```python
# Developed By:K.Jhansi

# Register Number:212221230045

# Write your code to find the histogram of gray scale image and color image channels.

import cv2

import matplotlib.pyplot as plt

gray_image = cv2.imread('grayscalerose.webp')

plt.imshow(gray_image)

plt.show()

color_image = cv2.imread('bird.webp')

plt.imshow(color_image)

plt.show()




# Display the histogram of gray scale image and any one channel histogram from color image

# Gray scale image

import cv2

import matplotlib.pyplot as plt

gray_image = cv2.imread('grayscalerose.webp')

plt.imshow(gray_image)

plt.show()

hist0 = cv2.calcHist([gray_image],[0],None,[256],[0,255])

plt.figure()

plt.title("Histogram")

plt.xlabel('grayscale value')

plt.ylabel('pixel count')

plt.stem(hist0)

plt.show()

# color image

import cv2

import matplotlib.pyplot as plt

color_image = cv2.imread('bird.webp')

plt.imshow(color_image)

plt.show()

hist1 = cv2.calcHist([color_image],[1],None,[256],[0,255])

plt.figure()

plt.title("Histogram of color_image - green channel")

plt.xlabel('intensity value')

plt.ylabel('pixel count')

plt.stem(hist1)

plt.show()



# Write the code to perform histogram equalization of the image. 

import cv2

gray_image = cv2.imread("grayscalerose.webp",0)

cv2.imshow('Grey Scale Image',gray_image)

equ = cv2.equalizeHist(gray_image)

cv2.imshow("Equalized Image",equ)

cv2.waitKey(0)

cv2.destroyAllWindows  






```
## Output:
### Input Grayscale Image and Color Image
![output](https://github.com/jhansi21005096/Histogram-of-an-image/blob/main/dipoutput-1.png)

### Histogram of Grayscale Image and any channel of Color Image
![output](https://github.com/jhansi21005096/Histogram-of-an-image/blob/main/dipoutput-2.png)
![output](https://github.com/jhansi21005096/Histogram-of-an-image/blob/main/dipoutput-3.png)
### Histogram Equalization of Grayscale Image
![output](https://github.com/jhansi21005096/Histogram-of-an-image/blob/main/dipoutput-4.png)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
