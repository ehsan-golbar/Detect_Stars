# Detect_Stars 🌟

## Project Overview
This project processes an input text file containing pixel values, converts it into an image, detects stars within the image, and generates a report with the number and coordinates of detected stars.

---

## Workflow

### 1. Convert Text File to Image
This step reads an input text file and creates an image from the pixel values:
- Extracts width, height, and RGB pixel data.
- Constructs an RGB image.
- Saves the image as `output_image.png`.

### 2. Generate Star Mask
This step processes the image to isolate stars:
- Converts the image to grayscale.
- Enhances contrast using adaptive histogram equalization.
- Applies binary thresholding.
- Cleans noise using morphological operations.
- Detects contours and filters by size.
- Saves the binary mask as `filtered_stars_mask.jpg`.

### 3. Count and Report Star Coordinates
This step analyzes the mask to count and locate stars:
- Loads the binary mask.
- Labels connected components to count stars.
- Extracts and prints star coordinates.

---

## Outputs
- `output_image.png`: Image generated from text file.
- `filtered_stars_mask.jpg`: Binary mask highlighting detected stars.
- Console output: Number of detected stars and their coordinates.

---

## Requirements
Ensure you have the following Python packages installed:
- `opencv-python`
- `numpy`
- `scipy`
- `Pillow`
- `scikit-image`

You can install the required packages using:
```bash
pip install opencv-python numpy scipy Pillow scikit-image

