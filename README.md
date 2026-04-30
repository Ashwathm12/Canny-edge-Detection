# Workshop 3 Canny-edge-detection
## Name: Ashwath M
## Register number: 212223230023

## Aim

To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

---

## Software Required

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (cv2)  
- NumPy  
- Matplotlib  

---

## ⚙️ Algorithm

### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load an image using `cv2.imread()`.

### Step 3:
Convert the image to grayscale.

### Step 4:
Apply **Sobel operator** using OpenCV to detect edges.

### Step 5:
Apply **Prewitt operator** using custom kernels.

### Step 6:
Apply **Roberts operator** using custom kernels.

### Step 7:
Apply **Laplacian operator** using OpenCV.

### Step 8:
Apply **Canny edge detector** using OpenCV.

### Step 9:
Display all edge-detected images for comparison.

---

## Program:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt

img=cv2.imread('dog.jpg')
img1=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
plt.imshow(img1)

img_gray=cv2.imread('dog.jpg',0)
plt.imshow(img_gray,cmap='gray')
plt.show()

np.max(img_gray)/2

edges= cv2.Canny(img_gray, threshold1=128, threshold2=128)
plt.imshow(edges,cmap='gray')

blurred_img=cv2.blur(img1,ksize=(3,3))
plt.imshow(blurred_img)

medium=np.median(img1)
medium

low=int(max(0,0.7*medium))
high=int(max(255,1/3*medium))

canny_edges_blur=cv2.Canny(blurred_img,threshold1=low,threshold2=high)
plt.imshow(canny_edges_blur)


```


---

## Output

###  Sobel Edge Detector
<img width="531" height="480" alt="image" src="https://github.com/user-attachments/assets/2ad7d9ea-fca7-48cd-b2f1-1fd8f2d3add3" />


###  Prewitt Edge Detector
<img width="500" height="482" alt="image" src="https://github.com/user-attachments/assets/5e7b9f1f-b101-4293-a448-2e9f58d232fe" />
 

###  Roberts Edge Detector
<img width="504" height="473" alt="image" src="https://github.com/user-attachments/assets/19f6c673-a2be-4f92-83be-c2a2340beba2" />
 

###  Laplacian Edge Detector
<img width="523" height="473" alt="image" src="https://github.com/user-attachments/assets/37d89fac-b24c-4fbb-a5f6-af18ed84d501" />
 

###  Canny Edge Detector
<img width="518" height="470" alt="image" src="https://github.com/user-attachments/assets/ca4d55f2-f880-4472-b5c5-2ab0b5db8c2b" />

---

## Result

Thus, edges are successfully detected using Sobel, Prewitt, Roberts, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
