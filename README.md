# OPENING-AND-CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.

### Step 2:
Create the Text using cv2.putText.

### Step 3:
Create the structuring element.

### Step 4:
Use Opening operation.

### Step 5:
Use Closing Operation.

### Step 6:
Print the output and end the program.
## PROGRAM:
Developed by : Javith farkhan S

Register number : 212221240017
### Import the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```python
text_image = np.zeros((100,190),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Javith",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')
```
### Create the structuring element
```python
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```

### Use Opening operation
```python
opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image,'magma')
plt.axis('off')
```
### Use Closing Operation
```python
closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image,'magma')
plt.axis('off')
```

## OUTPUT:

### Input Image

![Di11 1](https://github.com/Javith-farkhan/Opening-and-Closing/assets/94296805/02c7cbc5-9220-43c7-bd04-936c25214bb8)


### Result of Opening

![Di11 2](https://github.com/Javith-farkhan/Opening-and-Closing/assets/94296805/c7d15346-434f-4094-a436-cd2d203c20c3)


### Result of Closing

![Di11 3](https://github.com/Javith-farkhan/Opening-and-Closing/assets/94296805/5b52e5ef-93a1-4342-b888-9fd5851f93d1)


## RESULT:
Thus, the Opening and Closing operation is used in the image using python and OpenCV.
