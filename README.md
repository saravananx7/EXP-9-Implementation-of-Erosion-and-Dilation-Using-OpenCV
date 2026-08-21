# EXP-9-Implementation-of-Erosion-and-Dilation-Using-OpenCV
## Aim
To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

## The program performs the following operations:

Image Erosion
Image Dilation
## Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
## Algorithm
## Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

## Step 2:
Create a blank image using NumPy.

## Step 3:
Insert text onto the image using OpenCV's text drawing function.

## Step 4:
Display the original image.

## Step 5:
Create a structuring element (kernel) of suitable size.

## Step 6: Image Erosion
Apply the erosion operation using the created kernel.
Remove pixels from the boundaries of foreground objects.
Display the eroded image.
## Step 7: Image Dilation
Apply the dilation operation using the same kernel.
Add pixels to the boundaries of foreground objects.
Display the dilated image.
## Step 8:
Compare the original, eroded, and dilated images.

## Program
## ORIGINAL IMAGE

```

import cv2
import matplotlib.pyplot as plt
img = cv2.imread("mount.jpg")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()

```
## EROSION
```

kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
erosion = cv2.erode(img, kernel, iterations=1)
plt.imshow(erosion, cmap="gray")
plt.title("Image Erosion")
plt.axis("off")
plt.show()
```
## DILATION
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
dilation = cv2.dilate(img, kernel, iterations=1)
plt.imshow(dilation, cmap="gray")
plt.title("Image Dilation")
plt.axis("off")
plt.show()
```
## Developed By
## Name: SARAVANAN K

## Register No: 212225040387

## Output
## Original Image
A text image containing characters is displayed.
The image serves as the input for morphological processing.
<img width="682" height="354" alt="image" src="https://github.com/user-attachments/assets/527b6550-9281-47c8-9c2c-36bd928ef642" />

## Erosion
Original image is displayed.
Eroded image is displayed.
The thickness of the characters is reduced.
Object boundaries shrink inward.
<img width="655" height="351" alt="image" src="https://github.com/user-attachments/assets/38094507-347e-449e-b5d0-2f950cffcb80" />

## Dilation
Original image is displayed.
Dilated image is displayed.
The thickness of the characters increases.
Object boundaries expand outward.

<img width="639" height="359" alt="image" src="https://github.com/user-attachments/assets/0d2f6a58-5d26-4589-928e-ae2aa8166103" />


## Result
Thus, the morphological operations Erosion and Dilation are successfully implemented using OpenCV.
