# EX03 Histogram-of-an-images
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
```
Developed By: Bharathganesh S
Register Number: 212222230022
```
```
import cv2
from matplotlib import pyplot as plt

image = cv2.imread('image03.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])


equalized_image = cv2.equalizeHist(gray_image)

plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])





```
## Output:
### Input Grayscale Image and Color Image

![image](https://github.com/user-attachments/assets/7d1f1df0-ff2b-4fb2-befd-7b9eb2d62453)

![Screenshot 2024-10-01 104800](https://github.com/user-attachments/assets/f8a9c180-1cee-4a4d-819d-c51ce5f0a99f)

### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/user-attachments/assets/e02cb4e5-dd17-4f58-9d27-47703a169151)



### Histogram Equalization of Grayscale Image.

![image](https://github.com/user-attachments/assets/ad7a6884-fbab-49ba-9a0a-ad3662720cd8)


![image](https://github.com/user-attachments/assets/2b26cd22-53d8-4571-a3e6-b5f4e907a157)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
