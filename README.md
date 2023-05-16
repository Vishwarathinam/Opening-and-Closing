### Opening-and-Closing

### Aim:
To implement Opening and Closing using Python and OpenCV.

### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
### Step 1:
Load the necessary packages requiured for the implemtation of opening and closing.

### Step 2:
Create the text image for the implemtation of opening and closing using cv2.putText function.

### Step 3:
Create the structuring image for the implemtation of opening and closing on the text image.

### Step 4:
Apply the erosion and dilation to the text image using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step 5:
Display the images of the erosion and dilation applied using the plt.imshow.

### Step 6:
End the program.
 
### Program:
```

Developed by : Vishwa Rathinam. S
Register Number: 212221240063
Program to implement Opening and Closing using Python and OpenCV.
```
```

# Import the necessary packages...

import cv2
import numpy as np
import matplotlib.pyplot as plt

```
```
# Create the Text using cv2.putText...

text_image = np.zeros((100,600),dtype = 'uint8')
font = cv2.FONT_HERSHEY_DUPLEX = 2
cv2.putText(text_image,"Vishwa Rathinam",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Text Image")
plt.imshow(text_image,'magma')
plt.axis('off')
```

```
# Create the structuring element...

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))
```

```
# Use Opening operation...

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Implementing Opening")
plt.imshow(image1,'magma')
plt.axis('off')
```


```
# Use Closing Operation...

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Implementing Closing")
plt.imshow(image2,'magma')
plt.axis('off')

```
## Output:

### Display the input Image
![v1](https://github.com/Vishwarathinam/Opening-and-Closing/assets/95266350/8790f032-b357-4b28-934d-9c2d1667b6a7)


### Display the result of Opening
![v2](https://github.com/Vishwarathinam/Opening-and-Closing/assets/95266350/43b3f68a-e60d-405b-8efe-dcd60bd91cd6)


### Display the result of Closing
![v3](https://github.com/Vishwarathinam/Opening-and-Closing/assets/95266350/97ef4ba5-fe04-47ec-893e-04e776d50454)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
