# Color Quantization

This project demonstrates the process of reducing the number of colors in an image using K-means clustering. The image is processed to find the most dominant colors and reduce the number of unique colors, which is often used in applications like image compression or creating stylized visuals.
## Features

    K-means Clustering: Uses K-means algorithm to find the main color clusters in the image.
    Color Reduction: Reduces the number of colors in the image to a specified number by clustering similar colors.
    Visual Output: Displays the original and color-quantized image with fewer colors.

## Requirements

This project requires Python 3.x and the following libraries:

    numpy
    matplotlib
    scikit-learn

You can install these dependencies using pip:

pip install numpy matplotlib scikit-learn

Installation

    Clone this repository to your local machine.

git clone https://github.com/yourusername/color-quantization.git
cd color-quantization

Install the required dependencies.

    pip install -r requirements.txt

    Make sure to place the image (palm_trees.jpg in this case) in the project directory or update the code to point to the correct file path.

## Usage

    Place your image in the directory or specify the path in the code.

    Run the script.

    python color_quantization.py

    The script will display the original image and the color-quantized image with reduced colors based on K-means clustering.

## Code Explanation
1. Image Loading and Preprocessing

        The image is loaded as a 3D array using matplotlib.image.imread().
        The image array is reshaped from 3D (height, width, channels) to 2D (height * width, channels) to prepare it for clustering.

2. K-means Clustering

        The KMeans model from sklearn.cluster is used to find n_clusters number of dominant colors in the image.
        The model is trained on the reshaped 2D image data.

3. Predicting Cluster Labels

        Each pixel in the image is assigned to the nearest cluster center using the trained K-means model.
        The cluster centers (dominant colors) are rounded to integers and used to replace the original colors of the image.

4. Reshaping and Displaying the Output

        The final image is reshaped back into 3D to match the original dimensions and displayed using matplotlib.
