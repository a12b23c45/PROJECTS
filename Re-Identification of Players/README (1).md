
#  Re-Identification in a Single Feed

This project focuses on real-time player re-identification and tracking from a single video feed of a football game. Using a provided 15-second video and a fine-tuned YOLOv11 model, the objective is to assign unique IDs to each player during the initial seconds of the video and maintain consistent identities even when players temporarily leave and re-enter the frame. 


## Objective
Identify and detect players using the provided YOLOv11 model.

Assign consistent IDs to each player based on their appearance in the initial few seconds.

Ensure same ID is retained when players reappear later in the video.

The final solution must simulate real-time player tracking and re-identification.

## How to Set Up and Run the Code

This guide explains how to run the player re-identification project using YOLOv11 and Deep SORT for tracking.

---

### Prerequisites

Ensure you have the following:

- A Google Drive account
- Files:
  - `best.pt` (YOLOv11 model) [Link](https://drive.google.com/file/d/1-5fOSHOSB9UXYPenOoZNAMScrePVcMD/view)
  - `15sec_input_720p.mp4` (15-second test video)

---

###  1. Upload Files to Google Drive

Create a folder in your Google Drive called `ReID_Project` and upload:

- `best.pt`
- `15sec_input_720p.mp4`

---

### 2. Install Required Packages

In Google Colab, run the following:

```bash
!pip install ultralytics deep_sort_realtime opencv-python

from ultralytics import YOLO

from deep_sort_realtime.deepsort_tracker import DeepSort
