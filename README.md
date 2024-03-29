# CS5330Lab1: Sky Pixel Identification Demo using Gradio
This repository contains a Google Colab notebook script for identifying sky pixels in an image using Gradio. The script leverages computer vision techniques to extract the sky region and provides a user-friendly interface for easy experimentation.

## Files
- **sky_pixel.ipynb**: Main Google Colab Notebook file containing the project code.
- **test_sky_pixel.ipynb**: Test file for validating the functionality of the project using images in the test_sky folder. Results are displayed directly in the notebook.
- **test_sky**: Image folder containing 20 images containing sky in different conditions(e.g., clear, cloudy, sunrise, sunset).
- **README.md**: Project documentation.

## Instructions
### Running on Google Colab
Ensure you have the necessary libraries installed before running the script. You can install them using the following command:
```
!pip install gradio
```

## Usage
1. Mount Google Drive: For accessing images.
```
from google.colab import drive
drive.mount('/content/drive', force_remount=True)
```

2. Run the script: Execute the script with the provided functions.

3. Visualize Sky Region: Use the get_sky_region function to visualize the identified sky region in a given image.

4. Interactive Interface: Utilize the Gradio interface to interactively identify sky pixels in real-time.
Launch the Gradio interface by running demo.launch() in the sky_pixel file.
```
# Define the Gradio interface
demo = gr.Interface(
    fn=gr_sky_region_extraction,
    inputs="image",
    outputs="image",
    title="Sky Pixel Identification",
    description="Result： Light part indicates sky pixels, dark for non-sky",
    allow_flagging="never",
    live=True,
    )

# Launch the Gradio interface
demo.launch()
```
Alternatively, running on public URL: https://fb3736638c5a8fd99f.gradio.live/

Sample result：
![Images/example.png](https://github.com/yiwenxu76/CS5330Lab1/blob/6a5c59e300f1e7b8e98f72e49c39e8d25c32803c/Sample%20Result.png)
