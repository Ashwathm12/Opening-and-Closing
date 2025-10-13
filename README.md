# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:

Create the structuring element.
### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program:
### DEVELOPED BY: Karan A
### REGISTER NO: 212223230099

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
image = np.zeros((600, 600), dtype=np.uint8)
cv2.putText(image,text='KARAN A',org=(40,300),fontFace=cv2.FONT_HERSHEY_SIMPLEX,fontScale=4,color=(255,255,255),thickness=25,lineType=cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.axis('off') 
plt.show()
```

# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```

## Output:

### Display the input Image

<img width="389" height="389" alt="image" src="https://github.com/user-attachments/assets/11fda5cd-c6f0-4f8e-9c91-ec9f17388dd0" />



### Display the result of Opening
<img width="515" height="110" alt="image" src="https://github.com/user-attachments/assets/42793805-9a1f-4451-a320-fc9131778f94" />



### Display the result of Closing
<img width="515" height="110" alt="image" src="https://github.com/user-attachments/assets/d313de5f-92ad-496a-9908-656e1cfdd533" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
