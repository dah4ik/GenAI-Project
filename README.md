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

📈 Success Metrics

The performance of the model is measured using standard computer vision benchmarks:

Metric,                               Value

mAP@0.5:                                       0.512,  

Precision:                                     0.485,  

Recall:                                        0.548, 

Results:![val_batch1_labels](https://github.com/user-attachments/assets/5f946115-e857-4fbb-9058-ed2edd862dcb)
<img width="512" height="466" alt="image" src="https://github.com/user-attachments/assets/4dd5aaa2-9220-4dc2-8f5f-4056c620a7a1" />
<img width="2400" height="1200" alt="results" src="https://github.com/user-attachments/assets/d919f224-34a0-41d1-89e3-62aaf693bc5c" />

<img width="2250" height="1500" alt="BoxP_curve" src="https://github.com/user-attachments/assets/12b29033-6543-40e2-b517-33eb003d395f" />

👥 Authors

Gonko Daniel

Gavris Svetlana

Semion Ostrovsky

