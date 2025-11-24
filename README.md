# EXP-10-OPENING--AND-CLOSING
### Name - Subikshan P
### Register Number - 212223240161
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:
```
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((300, 600), dtype='uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, "Kamesh", (5, 150), font, 3, (255), 5, cv2.LINE_AA)
cv2.imshow("Original", img)
cv2.waitKey(0)

# Create the structuring element
kernel_open = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
kernel_close = cv2.getStructuringElement(cv2.MORPH_RECT, (11, 11))

# Use Opening operation
opened = cv2.morphologyEx(img, cv2.MORPH_OPEN, kernel_open)
cv2.imshow("Opening", opened)
cv2.waitKey(0)

# Use Closing Operation
closed = cv2.morphologyEx(img, cv2.MORPH_CLOSE, kernel_close)
cv2.imshow("Closing", closed)
cv2.waitKey(0)
```
## Output:

### Display the input Image
<img width="743" height="378" alt="image" src="https://github.com/user-attachments/assets/2bed7cd4-ea87-4213-9632-a98eadeb00b1" />



### Display the result of Opening
<img width="745" height="407" alt="image" src="https://github.com/user-attachments/assets/9bc0fcf4-2431-4e63-9394-6fdbe5384142" />




### Display the result of Closing
<img width="741" height="410" alt="image" src="https://github.com/user-attachments/assets/269a47c9-a1a0-48cf-9953-735ebc2b7fc2" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
