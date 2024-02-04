# CS5330Lab1: Sky Pixel Identification Demo using Gradio
This repository contains a Google Colab notebook script for identifying sky pixels in an image using Gradio. The script leverages computer vision techniques to extract the sky region and provides a user-friendly interface for easy experimentation.

## Files
- **sky_pixel.ipynb**: Main Google Colab Notebook file containing the project code.
- **test_sky_pixel.ipynb**: Test file for validating the functionality of the project using 20 sky images in different conditions. Results are displayed directly in the notebook.
- **README.md**: Project documentation.

## Instructions
### Running on Google Colab
Ensure you have the necessary libraries installed before running the script. You can install them using the following command:
"""
!pip install gradio
"""

## Usage
1. Mount Google Drive: For accessing images.
"""
from google.colab import drive
drive.mount('/content/drive', force_remount=True)
"""

2. Run the script: Execute the script with the provided functions.

3. Visualize Sky Region: Use the get_sky_region function to visualize the identified sky region in a given image.

4. Interactive Interface: Utilize the Gradio interface to interactively identify sky pixels in real-time.
Launch the Gradio interface by running demo.launch().
Running on public URL: https://b5e2a0b6b9f1184d36.gradio.live
