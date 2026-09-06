# Exp-9--Record-IMPLEMENTATION-OF-EROSION-AND-DILATION
## Name : SHRIHARI M
## Reg.no : 212225230265
## Aim
To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

Image Erosion
Image Dilation
## Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
##cAlgorithm
Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

Step 2:
Create a blank image using NumPy.

Step 3:
Insert text onto the image using OpenCV's text drawing function.

Step 4:
Display the original image.

Step 5:
Create a structuring element (kernel) of suitable size.

Step 6: Image Erosion
Apply the erosion operation using the created kernel.
Remove pixels from the boundaries of foreground objects.
Display the eroded image.
Step 7: Image Dilation
Apply the dilation operation using the same kernel.
Add pixels to the boundaries of foreground objects.
Display the dilated image.
Step 8:
Compare the original, eroded, and dilated images.
## Program
```
Original Image
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("image.png")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()

Erosion
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
erosion = cv2.erode(img, kernel, iterations=1)
plt.imshow(erosion, cmap="gray")
plt.title("Image Erosion")
plt.axis("off")
plt.show()

Dilation
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
dilation = cv2.dilate(img, kernel, iterations=1)
plt.imshow(dilation, cmap="gray")
plt.title("Image Dilation")
plt.axis("off")
plt.show()
```

## Output:
<img width="575" height="401" alt="image" src="https://github.com/user-attachments/assets/d40975a6-b2d6-4fb0-9a8e-7ea505f57fb0" />

<img width="576" height="393" alt="image" src="https://github.com/user-attachments/assets/545fccb2-351d-4ea0-b17a-b37a01c81a33" />

<img width="590" height="390" alt="image" src="https://github.com/user-attachments/assets/cd6788a4-a4c1-46bb-805b-e5bacfbb524a" />

## Result
Thus, the morphological operations Erosion and Dilation are successfully implemented using OpenCV.
