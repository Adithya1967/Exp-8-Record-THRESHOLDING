# Exp-8-Record-THRESHOLDING
# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name:** Adithya Sivakumar

**Register No:** 212224040013

## Output
### Original Image
```
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("dipt.jpg")

if img is None:
    print("Error: Image not found. Check the file path.")
else:
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    plt.imshow(img_rgb)
    plt.title("Original Image")
    plt.axis("off")
    plt.show()
```

<img width="185" height="209" alt="download" src="https://github.com/user-attachments/assets/f6060733-f04a-4196-bed7-76b65deeb72d" />



### Original Grayscale Image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Grayscale Image")
plt.axis("off")
plt.show()
```

<img width="384" height="410" alt="image" src="https://github.com/user-attachments/assets/483d1369-4cee-436c-96a2-1bb47f903009" />



### Global Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```

<img width="294" height="301" alt="image" src="https://github.com/user-attachments/assets/93e03106-c5d7-43e6-a772-94cf1ee6bd7e" />



### Adaptive Thresholding

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
result = cv2.adaptiveThreshold(
    img, 255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11, 2
)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()
```

<img width="318" height="303" alt="image" src="https://github.com/user-attachments/assets/cc4b7b9c-3048-4d39-8756-75a894ac4c03" />


### Otsu's Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```

<img width="284" height="294" alt="image" src="https://github.com/user-attachments/assets/6b977989-6e6d-4a26-a3be-9a564e6f75d9" />



## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
