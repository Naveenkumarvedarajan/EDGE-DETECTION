# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('F1.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
# Original Image
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
<img width="227" height="411" alt="2112266b-9f73-4a60-b51d-338fecc74810" src="https://github.com/user-attachments/assets/3b1c632e-01be-43bf-8e8a-b504fd23eef5" />



### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="227" height="411" alt="e446855d-9020-45a8-a04c-1fa2abbdf60f" src="https://github.com/user-attachments/assets/2872dcd7-adae-4d76-bfc7-b0b184ff5e16" />

### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="231" height="411" alt="35b73bf0-537d-408d-a7ca-46d530c611e4" src="https://github.com/user-attachments/assets/d24b0ce2-5610-4ec5-9c54-c179f8701e66" />

### CANNY EDGE DETECTOR

canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
<img width="227" height="411" alt="dbb970ab-44e8-4420-95a7-690eea48f03a" src="https://github.com/user-attachments/assets/b725b666-7c39-4fd1-8a47-2fd58034e4c7" />




## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
