# Drowsiness Detection System

A Python-based application for real-time drowsiness detection to enhance safety by monitoring eye closure and blink patterns via webcam.

## Overview

This system leverages computer vision techniques to detect facial features and monitor eye activity. It calculates blink rates and triggers alerts when prolonged eye closure indicates potential drowsiness, helping prevent accidents in driving or operational scenarios.

## Key Features

- **Real-time Monitoring:** Continuous analysis of webcam feed for face and eye detection.
- **Blink Tracking:** Measures blink rate per minute.
- **Drowsiness Alerts:** Visual warnings when eyes remain closed beyond the threshold (2 seconds).
- **User-friendly Interface:** Displays status, blink rate, and alerts on-screen.

## Technologies Used

- **Language:** Python 3.x
- **Libraries:**
  - OpenCV: For image processing and Haar cascade-based detection
  - NumPy: For efficient numerical operations
- **Machine Learning:** Utilizes pre-trained Haar cascade classifiers for face and eye detection, based on AdaBoost algorithm.

## Prerequisites

- Python 3.x installed
- Webcam connected to the system

## Usage

1. Run the application:
   ```
   python main.py
   ```

2. The system will access your webcam and start monitoring.

3. View the live feed with detection rectangles and status information.

4. Press 'q' to exit the program.

## How It Works

- Captures video from the webcam at 1280x720 resolution.
- Applies Haar cascades to detect faces and eyes in each frame.
- Computes total eye area to determine if eyes are open or closed.
- Tracks eye closure duration; alerts if exceeds 2 seconds.
- Distinguishes between normal blinks (< 0.3 seconds) and drowsiness.
- Updates blink rate every minute and displays metrics in real-time.

## Project Structure

- `main.py`: Core script containing the detection logic.
- `requirements.txt`: List of Python dependencies.
- `README.md`: This documentation file.

