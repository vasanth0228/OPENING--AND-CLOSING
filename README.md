# IMPLEMENTATION-OF-OPENING-AND-CLOSING
## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
**Step-1:**

Import the necessary packages

**Step-2:**

Create the Text using cv2.putText

**Step-3:**

Create the structuring element

**Step-4:**

Use Opening operation

**Step-5:**

Use Closing Operation

 
## Program:
```
Developed by: Vasanth kumar V
Reg.No: 230502027
```

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Load the image using cv2.imread()
image = cv2.imread("Fish.jpg")  

# Step 2: Create a structuring element (5x5 rectangular)
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Plot the original, opening, and closing images using Matplotlib
plt.figure(figsize=(10, 5))

plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

```

### Display the input Image:

<img width="512" height="409" alt="image" src="https://github.com/user-attachments/assets/7fad6a1a-718a-49dd-a6fd-0ceb0412d56d" />


<br>

```python
# Step 3: Use Opening operation (erosion followed by dilation)

opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)

plt.subplot(1, 3, 2)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```

### Display the result of Opening:

<img width="519" height="410" alt="image" src="https://github.com/user-attachments/assets/eef4d418-daa5-4bf0-8e74-ed9f03b2f416" />


<br>

```python
# Step 4: Use Closing operation (dilation followed by erosion)

closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
# Convert images from BGR to RGB for Matplotlib
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 3, 3)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")

plt.tight_layout()
plt.show()

```
### Display the result of Closing:


<img width="507" height="418" alt="image" src="https://github.com/user-attachments/assets/8ab0cf57-c87d-4e7f-96e8-0f6d3ef652d7" />


<br>
## Result:
Thus,the Opening and Closing operation is used in the image using python and OpenCV.
