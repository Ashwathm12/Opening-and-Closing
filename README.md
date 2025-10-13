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
### DEVELOPED BY: Ashwath M
### REGISTER NO: 212223230023

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
image = np.zeros((600, 600), dtype=np.uint8)
cv2.putText(image,text='Ashwath',org=(40,300),fontFace=cv2.FONT_HERSHEY_SIMPLEX,fontScale=4,color=(255,255,255),thickness=25,lineType=cv2.LINE_AA)
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
image_open = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open,cmap='gray')
plt.axis("off")
plt.show()


```
# Use Closing Operation
```
image_close = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close,cmap='gray')
plt.axis("off")
plt.show()

```

## Output:

### Display the input Image

<img width="442" height="425" alt="image" src="https://github.com/user-attachments/assets/24e656d2-e3aa-403f-a026-d5f35c4639a8" />




### Display the result of Opening
<img width="462" height="442" alt="image" src="https://github.com/user-attachments/assets/906213a6-fc33-4585-a054-4a30093aedbc" />




### Display the result of Closing
<img width="426" height="426" alt="image" src="https://github.com/user-attachments/assets/35d53bf3-9a9b-4782-9852-892ad110b782" />




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
