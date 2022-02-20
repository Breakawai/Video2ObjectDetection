# Video2ObjectDetection
This repo contains a lighter version of the *"Video2ObjectDetection"* prototype that allows the extraction of events in the turnaround process of the airport. 

The code was inspired by the [YOLO](https://github.com/pjreddie/darknet) repository. 
 
## Requirements
Tested with Python 3.9. Install the necessary packages with
```bash
pip install -r requirements.txt
```

## Download of the weights file
The weights file is the neural network model trained specifically for the turnaround process, with airport objects. 
The model can be downloaded at the following link: 
<https://drive.google.com/drive/folders/1MjeCrXIQclk0y9LlL--hWrUvUXPTHaEx>

## Download examples of turnaround videos
There is a shortlist of turnaround airport videos available online. 
A list of youtube videos can be downloaded using the following:
<https://drive.google.com/drive/folders/1ZuBrpAuvPmQ4P5a-26dgpZMdPjBPwRvD?usp=sharing>

## Solution configuration
There are 2 configuration needed to be made before running the code:
* Video Stream HTTP Connection 
* Siddhi Stream HTTP Connection

This changes needs to be done on file *"Video2ObjectDetection.py"*:
```
# --------------------- CONFIGURATION ---------------------------------

VIDEO_STREAM_HTTP_CONNECTION = "http://localhost:8080/"

SIDDHI_STREAM_HTTP_CONNECTION = "http://localhost:8280/siddhi"

# ---------------------------------------------------------------------
```

## Video Configuration (VLC Stream)
To create an HTTP Connection using the VLC Stream you should follow the next steps:
1. Open VLC Media Player
2. Create a new stream connection (CTRL+S)
3. Add the turnaround video
4. Select the **HTTP** as a new destination
5. Add the port number: 8080 
6. Select a transcoding profile (usually we use a *"Video - MPEG-2 + MPGA (TS)"*)
7. Guarantee that the video codec has a Bitrate up to 20000 kb/s

## Domain 
This solution describes a process in a real-world environment by acquiring data from environments where that wouldn't be possible. 
The domain of this solution could be given by:
![solution_domain](https://user-images.githubusercontent.com/99749820/154712825-cf3bb91c-bd7a-491b-a35e-cd41ce65f19e.png)


# Prototype running printscreen
![printscreen-prototype_2](https://user-images.githubusercontent.com/99749820/154716291-4f5324e7-bf2b-492b-ab51-ef3fd69800c3.png)
