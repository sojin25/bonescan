# Image Analysis Script

[English](./README.md) | [日本語](./README_JA.md)

This project contains a Python script for comparing two images and analyzing the similarity of specific color regions (red and blue). It is designed to run in a Jupyter Notebook environment.

## Features

- Image alignment based on contours
- Segmentation of red and blue color regions
- Similarity calculation using Dice coefficient and Hausdorff distance
- Generation of overlay images visualizing matching and non-matching regions

## Requirements

- Python 3.6 or higher
- Jupyter Notebook

## Required Python Modules

The following Python modules are required:

- opencv-python (cv2)
- numpy
- scikit-image
- scipy
- matplotlib

You can install these modules using the following command:

```
pip install opencv-python numpy scikit-image scipy matplotlib
```

## Usage

1. Clone or download this repository.

2. Prepare two image files you want to compare and place them in the same directory as the script.
   - Default file names:
     - `0130000001-1_origin_output.png`
     - `0130000001-1_filter_output.png`
   - If you use different images, modify the `img1_path` and `img2_path` variables in the script accordingly.

3. Launch Jupyter Notebook:
   ```
   jupyter notebook
   ```

4. Create a new notebook and copy & paste the provided script content into a cell.

5. Run the cell. The results will display:
   - Dice coefficients for red and blue regions
   - Hausdorff distances for red and blue regions
   - Overlay images showing matching and non-matching areas

## Example

Here's an example of how the script works with actual images:

### Input Images

Image 1 (Origin):

![Origin Image](path_to_image1.png)

Image 2 (Filter):

![Filter Image](path_to_image2.png)

### Result Images

Comparison of Blue Regions:

![Blue Regions Comparison](path_to_image3.png)

Comparison of Red Regions:

![Red Regions Comparison](path_to_image4.png)

In the result images:
- Green areas indicate matching regions between the two input images.
- Red areas in Image 3 show blue regions that don't match between the inputs.
- Red areas in Image 4 show red regions that don't match between the inputs.

The script calculates Dice coefficients and Hausdorff distances for both red and blue regions, providing a quantitative measure of similarity between the two input images.

## Customization

- Adjusting color ranges: Modify the `lower_red1`, `upper_red1`, `lower_red2`, `upper_red2`, `lower_blue`, and `upper_blue` variables to change the color detection ranges.
- Overlay transparency: Change the `alpha` parameter in the `create_overlay_image_with_white_background` function to adjust the transparency of the overlay images.

## Notes

- Alignment and segmentation results may vary depending on the size and format of the images.
- Processing large images may take longer to execute.

## Troubleshooting

- If you encounter module import errors, ensure that the required modules are correctly installed.
- If you experience image loading errors, check that the file paths are correct and the image files exist.

If you have any questions or issues, please feel free to open an Issue.
