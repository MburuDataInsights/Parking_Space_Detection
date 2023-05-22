# Parking_Space_Detection

This repository contains a Python script for detecting parking spaces in a video feed. The script utilizes computer vision techniques to analyze frames from a video and determine the availability of parking spaces.

## Functionality
The parking space detection script performs the following steps:

Video Input: The script takes a video file (carPark.mp4) as input. You can replace it with your own video file if desired.

Preprocessing: Each frame of the video is processed to enhance the parking space detection. The preprocessing steps include converting the frame to grayscale, applying Gaussian blur, adaptive thresholding, median blur, and dilation.

Parking Space Detection: The script identifies parking spaces by analyzing each frame. It uses a predefined list of parking space positions (loaded from CarParkPos file) to check the occupancy of each parking space. If the number of non-zero pixels in a parking space region is below a certain threshold, it is considered as a free space. Otherwise, it is marked as occupied.

Visualization: The script draws rectangles around the parking spaces, indicating their availability. It also displays the count of free parking spaces out of the total available spaces.

Continuous Processing: The script continues processing each frame of the video until it reaches the end. If the end is reached, it starts again from the beginning.

## Customization
You can customize the functionality of the parking space detection script by modifying the following aspects:

Input Video: Replace the default video file (carPark.mp4) with your own video file by updating the file name in the script.

Parking Space Positions: Modify the CarParkPos file or use your own file to define the positions of parking spaces. Ensure that the file is in the appropriate format and contains the correct coordinates for each parking space.

Detection Thresholds: Adjust the detection thresholds and parameters within the script according to your requirements. This includes the threshold for counting non-zero pixels to determine parking space occupancy.

## Usage
### Clone the repository:

bash

git clone https://github.com/your-username/your-repository.git
Navigate to the project directory:

bash

cd your-repository
Place your video file in the project directory and update the script to use the correct video file name.

### Run the script:


python parking_detection.py
The script will process the video frames and display the result in a new window, showing the availability of parking spaces.
