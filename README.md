# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read two images, Color image and Gray Scale image.
<br>

### Step2:

Calculate the Histogram of Gray scale image and each channel of the color image.
<br>

### Step3:

Display the histograms with their respective images.
<br>

### Step4:

Equalize the grayscale image.
<br>

### Step5:

Display the grayscale image.
<br>

## Program:
```python
# Developed By: Pamalakula Deepika
# Register Number: 21221240035
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

gray_image=cv2.imread('gray.png')
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.imshow(gray_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image

color_image=cv2.imread('monkey.png')
hist=cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.imshow(color_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('colorscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

# Write the code to perform histogram equalization of the image. 

gray_image = cv2.imread('gray.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
<br>
<img width="408" alt="e1" src="https://user-images.githubusercontent.com/94154679/167075329-e93834f4-ea65-404f-ae5d-b8d2e226ff45.png">
<br>

### Histogram of Grayscale Image and any channel of Color Image
<br>
<img width="415" alt="e2" src="https://user-images.githubusercontent.com/94154679/167075352-5ec90098-4161-440e-86e8-fca585e11a78.png">
<br>

### Histogram Equalization of Grayscale Image
<br>
<img width="667" alt="e3_1" src="https://user-images.githubusercontent.com/94154679/167075382-55a39f66-5a0c-4f65-8d34-52d820fdde33.png">
<br>
<img width="668" alt="e3_2" src="https://user-images.githubusercontent.com/94154679/167075392-ead98d3c-ea83-47bb-9eeb-9d49da26ebcb.png">
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
