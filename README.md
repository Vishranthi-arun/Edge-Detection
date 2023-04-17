# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.
<br>


### Step2:
Read the image and convert the bgr image to gray scale image.
<br>

### Step3:
Use any filters for smoothing the image to reduse the noise.
<br>

### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.
<br>

### Step5:
Display the filtered image using plot and imshow.
<br>

 
## Program:
```
Developed by : Vishranthi A
Register No. 212221230124
```
``` Python
#IMPORT PAKAGES
import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
img = cv2.imread("burj.jpg")
plt.imshow(img)
gray_image = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)


# SOBEL EDGE DETECTOR

sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.imshow(sobelx)
plt.title("SOBEL_X")
plt.xticks([])
plt.yticks([])
plt.show()

sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.imshow(sobely)
plt.title("SOBEL_Y")
plt.xticks([])
plt.yticks([])
plt.show()

sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize =(8,8))
plt.imshow(sobelxy)
plt.title("SOBEL_XY")
plt.xticks([])
plt.yticks([])
plt.show()

# LAPLACIAN EDGE DETECTOR

laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.imshow(laplacian)
plt.title('LAPLACIAN')
plt.axis("off")
plt.show()

# CANNY EDGE DETECTOR

canny_edges = cv2.Canny(new_image,120,150)
plt.figure(figsize=(8,8))
plt.imshow(canny_edges)
plt.title('CANNY_EDGES')
plt.axis("off")
plt.show()

```
## Output:
### ORIGINAL IMAGE 
![image](https://user-images.githubusercontent.com/93427278/232553277-cbaf2601-a5e2-4dcb-bdff-609abfc2104d.png)

### SOBEL EDGE DETECTOR
![image](https://user-images.githubusercontent.com/93427278/232553368-2be674d6-2078-478d-9a82-bb97cf8bea44.png)

![image](https://user-images.githubusercontent.com/93427278/232553467-64093cd1-0673-4031-8452-20e950d70766.png)

![image](https://user-images.githubusercontent.com/93427278/232553571-795c0b29-1d12-4487-85f0-7357c60fbbc4.png)


### LAPLACIAN EDGE DETECTOR

![image](https://user-images.githubusercontent.com/93427278/232553674-3bb6d250-d44c-4147-b058-73143fabd98d.png)



### CANNY EDGE DETECTOR

![image](https://user-images.githubusercontent.com/93427278/232553763-7284419a-26fc-46cb-bd26-9536c58e36b3.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
