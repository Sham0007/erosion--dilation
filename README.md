# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages

### Step2:
create the text using cv2.put Text


### Step3:
create the structuting element


### Step4:
Erodde the image


### Step5:
Dilate the image


 
## Program:

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```



# Create a blank image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```


# Add text on the image using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Vinnusheh', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```


# Display the input image
```
plt.title("Input Image with Text")
plt.axis('off')
```



# Create a simple square kernel (3x3)
```
kernel = np.ones((3, 3), np.uint8)
```

# Apply erosion (shrinking effect)
```
eroded_image = cv2.erode(image, kernel, iterations=1)
```
# Display the eroded image
```
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```

## Output:

### Display the input Image
<img width="605" height="645" alt="image" src="https://github.com/user-attachments/assets/a1028cf4-d85a-4fe9-b3d4-0e8ad721a6d8" />

### Display the Eroded Image
<img width="603" height="642" alt="image" src="https://github.com/user-attachments/assets/b752fe13-6612-423a-ba50-655fb15a177b" />

### Display the Dilated Image
<img width="608" height="646" alt="image" src="https://github.com/user-attachments/assets/3f440638-a584-4b2d-8274-62d20b84d995" />

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
