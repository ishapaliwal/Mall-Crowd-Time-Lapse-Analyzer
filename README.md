# CrowdQuant: Advanced Computer Vision for Mall Traffic Analysis
_Harnessing the power of AI to decode complex crowd patterns in real-time._

## Developers:
Isha Paliwal (GWID: G49146952)

Needhi Kore (GWID: G20475943)

## Professor/s:
Robert Pless

## Understanding the Problem and Project Scope:
The **Mall Surveillance Time-Lapse Analyzer** is a Python tool made to evaluate mall surveillance time-lapse footage in order to examine crowd dynamics. The primary challenge addressed by this project is developing an analytical tool that leverages advanced computer vision techniques to calculate the number of people per frame in mall surveillance videos. The project's main application can be to provide mall management with an analytical tool that will help with operational planning and crowd control.

## Who Would Care?
Mall managers might use this tool to optimize security and staffing, retail managers could use it to modify operations based on customer flow, and safety officers could use it to develop emergency reaction plans. Furthermore, urban planners and researchers studying crowd dynamics could also find this tool beneficial.

## Python Script for Project:
The following Jupyter Notebook covers the complete workflow, from frame extraction and video processing to real-time crowd analysis, giving crucial information for improved operational planning.

[Counting_no_of_people.ipynb](https://github.com/ishapaliwal/Mall-Crowd-Time-Lapse-Analyzer/blob/main/Counting_no_of_people.ipynb)

## Steps to Execute:
Make sure all required files are properly configured in your project directory before beginning the analysis. To get ready to carry out the analysis, take the following actions:

1. Download YOLOv3 Weights:
  - Because of its size, the **yolov3.weights** file is too big to upload straight to GitHub. Use [this link](https://pjreddie.com/media/files/yolov3.weights) to download it instead.
  - The yolov3.weights file should be saved in the same folder as the code, the video, and any additional supporting files.
2. Prepare the Project Directory:
  - Ensure that the project directory contains the following files:
    - [american_mall_video.mp4](https://github.com/ishapaliwal/Mall-Crowd-Time-Lapse-Analyzer/blob/main/american_mall_video.mp4): Video file for analysis.
    - [coco.names](https://github.com/ishapaliwal/Mall-Crowd-Time-Lapse-Analyzer/blob/main/coco.names): Class identifier names used by YOLO.
    - [yolov3.cfg](https://github.com/ishapaliwal/Mall-Crowd-Time-Lapse-Analyzer/blob/main/yolov3.cfg): Configuration file for the YOLO model.
    - **yolov3.weights**: Weights for the YOLO model that was just downloaded.
    - [Counting_no_of_people.ipynb](https://github.com/ishapaliwal/Mall-Crowd-Time-Lapse-Analyzer/blob/main/Counting_no_of_people.ipynb): The Jupyter Notebook containing the project code.
3. Execute the Jupyter Notebook:
  - Open **Counting_no_of_people.ipynb** in a Jupyter environment.
  - Run all cells in the notebook to perform the video analysis, frame extraction, and crowd counting.

By taking these preparatory actions, you make sure that everything is ready for the crowd analysis tool to be used successfully.

## Our Approach:
Our study analyzes mall time-lapse security footage using the YOLO (You Only Look Once) deep learning model. The procedure is divided into multiple crucial steps:

1. **Frame Extraction**: We extract four frames per second from the video, which enables a thorough examination of how the crowd moves over time. This makes it easier to record even minute variations in crowd density and trends.
2. **People Detection**: The pre-trained YOLO model, which is renowned for its precision and effectiveness in real-time object detection, is used to process frames in order to identify individuals. To maximize the sensitivity and accuracy of detection, we modify the model's confidence threshold.
3. **Data Analysis**: The number of people identified in each frame is aggregated to evaluate patterns in crowd density, peak hours, and other pertinent data that may help guide security and operational plans in shopping centers.

## Challenges:
1. **Accuracy vs. Speed**: It's critical to strike a balance between detection accuracy and processing speed, particularly when examining high-resolution video data with fast frame rates.
2. **Environmental Variables**: We must modify our model parameters to account for variations in illumination, crowd density, and camera angles, which can impact detection reliability.
3. **Resource Intensity**: Handling and processing large video files demands significant computational resources, potentially limiting the scalability of our solution in less equipped environments.

## Tools and Resources
1. **Python**: The core programming language used for implementing our solution.
2. **OpenCV Library**: Utilized for video processing tasks, including reading video files, extracting frames, and interfacing with the YOLO model for object detection.
3. **YOLO (You Only Look Once)**: A state-of-the-art, real-time object detection system that identifies objects in images and video with high precision.

## Results:
The Mall Surveillance Time-Lapse Analyzer has proven effective in calculating the total number of people per frame, providing clear, frame-by-frame data that can be used to assess crowd density and flow trends. The final results, which detail the number of people counted in each frame, are stored in a text file named [results.txt](https://github.com/ishapaliwal/Mall-Crowd-Time-Lapse-Analyzer/blob/main/results.txt). Furthermore, the extracted frames can be seen directly in the GitHub repository's [frames](https://github.com/ishapaliwal/Mall-Crowd-Time-Lapse-Analyzer/tree/main/frames) directory, enabling visual confirmation and additional examination of particular moments caught in the security tape. This feature improves transparency and offers a useful tool for users who wish to take a closer look at the processed frames.

## Conclusion:
In conclusion, the project successfully meets the need for a technical solution that quantifies crowd size per frame in a mall surveillance setting. By focusing on individual frames, the tool provides detailed insights into crowd patterns, crucial for operational decisions and crowd management strategies. This frame-specific approach delivers actionable intelligence for each captured moment of the surveillance footage.
