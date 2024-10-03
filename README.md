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

# Developed By: vidhyasri
# Register Number: 212222230170
## FOR BRIGHT IMAGE
```
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Load the color image
image = cv2.imread('Bright.tif')

# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)

# Plotting the original grayscale image, equalized image, and histograms
plt.figure(figsize=(10, 7))

# Show original grayscale image
plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

# Show equalized grayscale image
plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
# Plot histogram of the original grayscale image
plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

# Plot histogram of the equalized image
plt.subplot(2, 2, 4)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()
```
## FOR DARK IMAGE
```
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Load the color image
image = cv2.imread('Dark.tif')

# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)

# Plotting the original grayscale image, equalized image, and histograms
plt.figure(figsize=(10, 7))

# Show original grayscale image
plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

# Show equalized grayscale image
plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

# Plot histogram of the original grayscale image
plt.subplot(2, 2, 3)
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

# Plot histogram of the equalized image
plt.subplot(2, 2, 4)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()
```

## Output:
## FOR BRIGHT IMAGE
![image](https://github.com/user-attachments/assets/1a3b74c0-d727-477a-8883-129bae10b656)

![image](https://github.com/user-attachments/assets/b666eac5-12a9-4290-b703-6b94c3a5b13c)

![image](https://github.com/user-attachments/assets/cc2b3127-9f28-4754-b06f-27e5c00af13c)

![image](https://github.com/user-attachments/assets/b0b8dfd9-2f9e-409d-bfb3-b79c5e0a0895)

## FOR DARK IMAGE
![image](https://github.com/user-attachments/assets/30826378-8534-4399-819a-9e18e7263c4e)

![image](https://github.com/user-attachments/assets/7160a7f0-2f30-478f-8ad0-9ef37e93ff3e)

![image](https://github.com/user-attachments/assets/fe98cc72-cff5-491e-a93b-dda937e5728a)

![image](https://github.com/user-attachments/assets/85a0055c-2ae7-4aea-bf33-ba9cf127a7c6)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
