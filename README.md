🛡️ Safeguarding Children's Spaces with AI Vision

This project focuses on an intelligent computer vision system designed to detect hazardous objects in children's environments before accidents happen, providing peace of mind for parents and caregivers.

📌 The Challenge

Parents and childminders face a constant struggle to identify dangerous objects hidden behind toys or lying on the floor.
Traditional data collection is limited due to privacy concerns in homes and the ethical impossibility of exposing children to real dangers for photography.

To solve this, we utilize synthetic data generation to create a robust, privacy-preserving training dataset, combining isolated objects and cluttered room scenes.

🚀 Hazard Detection Classes

The focus is on identifying four main classes of hazards:

Sharp Objects – knives and scissors that could cause cuts or puncture wounds 

Choking Hazards – small objects such as coins, small batteries, small balls, and Lego parts that could obstruct airways .

Electrical Hazards –  cables,  adapters, and  sockets.

Chemical Dangers – cleaning products, detergents, or any chemical bottles that could be ingested.

🛠 Methodology & Tools
Data Annotation and Refinement

To ensure high-quality training data and precise object boundaries, we employed:

CVAT (Computer Vision Annotation Tool) – for professional-grade labeling and managing the synthetic dataset.

SAM (Segment Anything Model) – for enhanced boundary refinement and precise instance segmentation of hazardous objects.

ML Architecture

The system uses cutting-edge object detection models to balance speed and accuracy:

YOLOv8 / YOLOv10 – optimized for real-time detection.

DETR / ViT-Det – transformer-based architectures for comparative analysis.

📊 Synthetic Data 

https://drive.google.com/drive/folders/15yNOOc1ldMNk8raNk40rbm8itB03Rnd_?usp=drive_link

🧠 Notebooks Overview
📘 Creating_and_marking_individual_objects_for_training.ipynb

This notebook focuses on creating isolated object images for each hazard class.

Approximately 100 images per class.

Each image contains a single object on a clean background.

Classes include:

Knives and scissors (Sharp Objects)

Coins, small batteries, small balls, Lego parts (Choking Hazards)

Exposed cables and adapters (Electrical Hazards)

Cleaning and chemical bottles (Chemical Dangers)

These images are used to:

Build a strong base detector.

Enable automatic or semi-automatic labeling.

Reduce the amount of manual annotation required.

🏠 01_generate_images.ipynb

This notebook generates synthetic images of full children’s rooms containing multiple hazardous objects.

Key characteristics:

Cluttered environments with toys and furniture.

Multiple hazard types in the same image.

Different lighting conditions and camera perspectives.

Due to scene complexity, only a selected subset of these images was:

Manually annotated using CVAT.

Used to fine-tune the model for real-world conditions.

🤖 02_train_yolo.ipynb

This notebook contains the full training pipeline for the detection model.

Model: YOLOv8

Input: Combination of

Isolated object images

Selected annotated room scenes

Output:

Trained weights saved in yolo_training/kids_room_hazard/weights/

Validation metrics (Precision, Recall, mAP)

This notebook represents the core learning stage of the project.

📊 Presentation
📎 Gen_AI_pres.pptx

📈 Success Metrics

The performance of the model is measured using standard computer vision benchmarks:

Metric,                               Value

mAP@0.5:                                       0.512,  

Precision:                                     0.632,  

Recall:                                        0.548, 

Results:![val_batch1_labels](https://github.com/user-attachments/assets/5f946115-e857-4fbb-9058-ed2edd862dcb)
<img width="512" height="466" alt="image" src="https://github.com/user-attachments/assets/4dd5aaa2-9220-4dc2-8f5f-4056c620a7a1" />
<img width="2400" height="1200" alt="results" src="https://github.com/user-attachments/assets/d919f224-34a0-41d1-89e3-62aaf693bc5c" />

<img width="2250" height="1500" alt="BoxP_curve" src="https://github.com/user-attachments/assets/12b29033-6543-40e2-b517-33eb003d395f" />

👥 Authors

Gunko Daniel

Gavris Svetlana

Semion Ostrovsky

