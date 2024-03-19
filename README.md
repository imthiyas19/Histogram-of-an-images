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
# Developed By: R.Thivakar
# Register Number: 212222240109
```
# Grayscale image and Color image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("immg.jpeg")
color_image = cv2.imread("img.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Histogram of Grayscale image and color image
```
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
# Histogram equalization of Grayscale image
```
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


![311955834-33ef503c-2ac2-4837-b296-4116f8f803d9](https://github.com/imthiyas19/Histogram-of-an-images/assets/120353416/688a489b-8e7d-4d0f-958e-ff9e4fad85ec)





### Histogram of Grayscale Image and any channel of Color Image



![311955899-8af5eb58-65ab-46b2-845e-36be7f8cd901](https://github.com/imthiyas19/Histogram-of-an-images/assets/120353416/46176eb3-6139-4ff9-9a50-4058477d2205)


![311955922-902d045a-a3dc-4d75-9f1c-2059cac663b8](https://github.com/imthiyas19/Histogram-of-an-images/assets/120353416/a71ceb71-408b-4a41-bb3a-3447f69ef45b)





### Histogram Equalization of Grayscale Image.




![311955948-bf7aafa7-d9b9-4f86-9926-9ef6c9d15c78](https://github.com/imthiyas19/Histogram-of-an-images/assets/120353416/e5ccd492-5576-4087-a864-bb353a2e7c69)







## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
