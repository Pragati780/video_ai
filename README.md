# Attribute-Based Person Retrieval System

## Overview

This project implements an end-to-end computer vision pipeline for locating individuals in videos based on visual attributes and generating the corresponding timestamp intervals.

The system processes video streams, detects people, extracts relevant visual features, and retrieves matching occurrences across the video timeline.

---

## Pipeline

Video Input
→ Frame Extraction
→ Frame Sampling
→ Person Detection (YOLOv8)
→ Person Cropping
→ Feature Extraction (HSV-based Color Analysis)
→ Person Retrieval
→ Timestamp Generation

---

## Project Statistics

* Video Length: ~2 minutes
* Total Frames: ~3500
* Sampling Rate: Every 10th frame
* Sampled Frames: ~350
* Person Crops Generated: ~1835

---

## Technologies Used

* Python
* OpenCV
* YOLOv8
* NumPy

---

## Methodology

### Frame Processing

* Read video using OpenCV.
* Extract frames and video metadata.
* Perform frame sampling for efficient processing.

### Person Detection

* Detect individuals using YOLOv8.
* Generate cropped person regions for further analysis.

### Feature Extraction

* Convert cropped images to HSV color space.
* Extract visual color-based features from the torso region.
* Compute feature scores for attribute matching.

### Retrieval & Localization

* Retrieve matching detections based on extracted features.
* Convert detected frame numbers into timestamps using video FPS.
* Merge nearby detections into continuous intervals.

---

## Future Improvements

* Multi-attribute retrieval
* Person Re-Identification using deep embeddings
* DeepSORT-based tracking
* CLIP / Vision-Language based attribute extraction
* Real-time video processing

