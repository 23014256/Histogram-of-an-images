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
# Developed By: SUMAN
# Register Number: 212223240163
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('a.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

equalized_image = cv2.equalizeHist(gray_image)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.figure(figsize=(10, 7))

plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

plt.subplot(2, 2, 4)
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()
```
  
## Output:
### Input Grayscale Image and Color Image
<img width="522" height="316" alt="Screenshot 2026-02-28 123709" src="https://github.com/user-attachments/assets/360fffc8-bc69-419b-afe8-461ca9eba3c5" />
<img width="396" height="312" alt="Screenshot 2026-02-28 123718" src="https://github.com/user-attachments/assets/b0695eaf-9db2-42ef-ab35-ab3519b96053" />




### Histogram of Grayscale Image and any channel of Color Image

<img width="563" height="362" alt="Screenshot 2026-02-28 123728" src="https://github.com/user-attachments/assets/089d6a6e-818f-4dbd-ac5f-dbbed06643ab" />





### Histogram Equalization of Grayscale Image.
<img width="531" height="345" alt="Screenshot 2026-02-28 123738" src="https://github.com/user-attachments/assets/78ec7041-4a29-4c06-83ab-6df4482c1715" />






## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
