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
cv2.putText(image, 'KESAVAN', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

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

<img width="757" height="550" alt="image" src="https://github.com/user-attachments/assets/833a21e4-8749-475d-80a3-cbbf59ab626c" />



Display the result of Opening

<img width="696" height="553" alt="image" src="https://github.com/user-attachments/assets/46dd0201-d881-4583-94d7-3c5e748d5a6c" />



Display the result of Closing

<img width="690" height="542" alt="image" src="https://github.com/user-attachments/assets/e07c22b7-6dca-4403-80c0-a310fe3606a8" />




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
