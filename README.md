## Ex 10- OPENING--AND-CLOSING

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
Anaconda - Python 3.7 

OpenCV
## Algorithm:
Step1:
Import the necessary packages

Step2:
Create the Text using cv2.putText

Step3:
Create the structuring element

Step4:
Use Opening operation

Step5:
Use Closing Operation

## Developed By
## Name: KESAVAN S
## Register Number: 212224230121

## Program:

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'AJAY', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

kernel = np.ones((3, 3), np.uint8)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')

# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')

```

## Output:
Display the input Image

<img width="665" height="506" alt="image" src="https://github.com/user-attachments/assets/422feb2f-fb43-40cb-9bca-c861372524a2" />


Display the result of Opening

<img width="659" height="524" alt="image" src="https://github.com/user-attachments/assets/fa1d326f-23ed-4d97-9926-4e98d43e20c0" />


Display the result of Closing

<img width="664" height="508" alt="image" src="https://github.com/user-attachments/assets/f7d0f30f-094c-428b-af19-2ec28ae448bb" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
