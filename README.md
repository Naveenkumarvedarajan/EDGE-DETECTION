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
![image]<img width="712" height="433" alt="Screenshot 2025-09-30 153330" src="https://github.com/user-attachments/assets/197cd83e-56fd-48aa-bedb-508fa4c210aa" />


### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="710" height="443" alt="Screenshot 2025-09-30 153337" src="https://github.com/user-attachments/assets/e327a368-d90b-49d4-be26-8970ef96f903" />

### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="734" height="451" alt="Screenshot 2025-09-30 153346" src="https://github.com/user-attachments/assets/85e7ef50-4a44-4b88-b471-49dc72b39823" />

### CANNY EDGE DETECTOR

canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  

<img width="804" height="439" alt="Screenshot 2025-09-30 153355" src="https://github.com/user-attachments/assets/a15b4ca8-1078-468d-93c6-157547b8fc36" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
