🔍 Project: Detection of Potentially Dangerous Objects in a Child’s Room

This project aims to automatically detect potentially dangerous objects in a children's room using Computer Vision and Generative AI.
The system identifies hazardous items such as batteries, scissors, pills, cables, and household chemicals based on room images.



📌 1. Motivation

Parents and caregivers cannot constantly monitor every corner of a room. Many dangerous objects are small, hard to notice, or blend into the environment.
Computer vision can help identify hazardous items and generate warnings before an accident occurs.



📌 2. Project Goal

Build and evaluate object-detection models capable of recognizing hazardous objects in a child’s room, comparing real data vs. synthetic data created using GenAI.



📌 3. Features

Synthetic image generation of rooms with hazardous objects

Object detection using YOLO

Comparison of datasets (real vs. synthetic vs. mixed)

Clear evaluation metrics (mAP, IoU, F1)


⚙️ 4. Installation

You can run the project on:

Google Colab (recommended)

Local machine (Windows/Linux/Mac)
_________________________________________________________________________________________________________________________________________________________________________

➡️ Install dependencies (Colab or local)

pip install ultralytics diffusers transformers accelerate safetensors opencv-python matplotlib


➡️ (Optional) Install PyTorch manually (local only)

pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118


