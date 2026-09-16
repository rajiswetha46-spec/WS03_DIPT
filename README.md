# Canny Edge Detection
## Name : SWETHA R
## Reg No: 212225100055
## Aim

To implement the **Canny Edge Detection** algorithm on a sample image and obtain the detected edges.

## Requirements

- Anaconda
- Jupyter Notebook
- Python
- OpenCV
- Sample Image

## Steps

1. Open **Jupyter Notebook** using Anaconda.
2. Read a sample image using OpenCV.
3. Convert the image into **grayscale**.
4. Apply the **Canny Edge Detection** algorithm.
5. Display the original image.
6. Display the detected edge image.
7. Change the threshold values and observe the output.

## Algorithm
```text
Sample Image
      ↓
Convert to Grayscale
      ↓
Canny Edge Detection
      ↓
Apply Threshold Values
      ↓
Detect Edges
      ↓
Display Edge Image
```

## Student Task

- Select a sample image of your choice.
- Apply the Canny Edge Detection algorithm.
- Display the detected edges.
- Perform the experiment with **3 different parameter settings**.
- Compare the results obtained using different threshold values.

## Discussion

Different parameter settings affect the number and strength of detected edges.

- **Low threshold values:** Detect more edges, including weak edges and noise.
- **Medium threshold values:** Detect clear and important edges.
- **High threshold values:** Detect mainly strong edges and remove weak edges.

## Program
```python
import cv2
import matplotlib.pyplot as plt

# Read the sample image
img = cv2.imread("sample.jpg")

# Convert image to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Apply Canny Edge Detection
edges = cv2.Canny(gray, 100, 200)

# Display original image
plt.subplot(1, 2, 1)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")

# Display detected edges
plt.subplot(1, 2, 2)
plt.imshow(edges, cmap="gray")
plt.title("Canny Edge Detection")
plt.axis("off")

plt.show()
```

## Parameter Settings

```python
# Parameter Setting 1
edges1 = cv2.Canny(gray, 50, 150)

# Parameter Setting 2
edges2 = cv2.Canny(gray, 100, 200)

# Parameter Setting 3
edges3 = cv2.Canny(gray, 150, 250)
```

## Output

- Original sample image

<img width="495" height="358" alt="Screenshot 2026-09-16 125637" src="https://github.com/user-attachments/assets/15ac7c43-2130-453d-bdc5-5fbb45fd7c24" />

- Canny edge-detected image
<img width="497" height="355" alt="Screenshot 2026-09-16 125742" src="https://github.com/user-attachments/assets/45cf699a-37f0-45c4-9b02-753d64ce6957" />

- Edge outputs for 3 different threshold settings
<img width="1215" height="274" alt="Screenshot 2026-09-16 125825" src="https://github.com/user-attachments/assets/cfd30bd7-2e11-4731-802d-c8c88a81aa24" />

## Result

The **Canny Edge Detection** algorithm was successfully implemented on the sample image, and the edges were detected using different parameter settings.
