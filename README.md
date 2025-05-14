# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Insert the text using cv2.putText()
- Step3: The perform the erosion for given text and display the text using imshow()
- Step4: Next,perform dilation for inout text and display the result
## Program:
```
DEVELOPED BY: DINESH KUMAR R
REGISTER NUMBER: 212222110010
```
### Import the necessary packages
```python
import cv2
import numpy as np 
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```python
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Dinesh',(5,70),font,2,(255),5,cv2.LINE_AA)
```
### Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
### Erode the image
```python
image_erode1=cv2.erode(img1,kernel1)
plt.imshow(image_erode1)
plt.axis("off")
```
### Dilate the image
```python
image_dilate1=cv2.dilate(img1,kernel1)
plt.imshow(image_dilate1)
plt.axis("off")
```
## Output:
### Display the input Image

![Screenshot 2024-04-17 085015](https://github.com/DINESH18032004/erosion--dilation/assets/119477784/cea23807-f3ea-4964-811c-24ea0635e11c)

### Display the Eroded Image

![Screenshot 2024-04-17 085027](https://github.com/DINESH18032004/erosion--dilation/assets/119477784/796db59d-705e-476e-bda0-8dd76c17ca8a)

### Display the Dilated Image

![Screenshot 2024-04-17 085103](https://github.com/DINESH18032004/erosion--dilation/assets/119477784/a1052338-f517-4846-a59f-c202593a7132)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
