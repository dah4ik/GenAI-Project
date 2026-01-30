# Safeguarding Children's Spaces with AI Vision 🚀

An intelligent computer vision system designed to detect hazardous objects in children's environments before accidents happen, providing peace of mind for parents and caregivers.

## 📂 Project Resources (Google Drive)
*Link to 2,000+ generated images and saved YOLOv8/v10 weights and exports.
* **[Full Synthetic Dataset]** —https://drive.google.com/drive/folders/1l5Z_nOrOzY2A1oY6fY6Cm-P2j8FH6YBf?usp=sharing 


---

## 👥 Project Team
* **Daniel Gonko**
* **Svetlana Gavris**
* **Semyon Ostrovsky**

---

## 📌 The Challenge
Parents and childminders face a constant struggle to identify dangerous objects hidden behind toys or lying on the floor. Traditional data collection is limited due to:
* **Privacy Concerns:** Collecting real images from private homes is invasive.
* **Ethical Barriers:** Exposing children to real dangers for photography is unacceptable.
* **Data Scarcity:** No existing open dataset focuses specifically on household hazards in children's rooms.

We utilize **Synthetic Data Generation (SDXL)** to create a robust, privacy-preserving training dataset.

---

## 🚀 Hazard Detection Classes
The system is trained to identify four critical categories:
1. **Choking Hazards** – Coins, small batteries,  and Lego parts.
2. **Sharp Objects** – Knives and scissors.
3. **Electrical Hazards** – Cables, adapters, and open sockets.
4. **Chemical Dangers** – Cleaning products, detergents, and chemical bottles.

---

## 🖼 Data Generation Examples
Samples of synthetic environments and individual objects created for the training pipeline.

| Synthetic Room Scene | Isolated Hazard Objects |
| :---: | :---: |
|![photo_2026-01-03_16-34-26](https://github.com/user-attachments/assets/4db4d844-ef44-4645-ae07-f8e6f0a479ce)|<img width="642" height="643" alt="image" src="https://github.com/user-attachments/assets/dd665eea-ea20-4101-a2ad-ce15d8debb11" />|
| *SDXL generated room with hidden hazards*
Sample prompt for this image:"Photorealistic nursery room, sharp scissors and a kitchen knife on a table, realistic shadows"| *100+ images per class for base detection* |

---

## 📊 Experimental Results & Comparison

### 1. Synthetic-Only Model
*Trained exclusively on 2,000+ AI-generated images.*

| Confusion Matrix (Synthetic) | Training Curves (Synthetic) |
| :---: | :---: |
|<img width="860" height="645" alt="image" src="https://github.com/user-attachments/assets/37ee9b72-7b41-4b73-b4da-ba82d68e764d" />|<img width="998" height="499" alt="image" src="https://github.com/user-attachments/assets/6bd9c8b1-d57b-4493-ba70-7c70ca2000c6" />|

**Analysis:** Shows the baseline performance and initial ability to recognize hazard shapes in clean environments.
| Output examples for individual objects | Output examples for room |
| :---: | :---: |
<img width="1200" height="1352" alt="image" src="https://github.com/user-attachments/assets/3491e7e0-c118-499e-bfeb-52f351336a9b" /> | <img width="1157" height="1156" alt="image" src="https://github.com/user-attachments/assets/a5f4e6a3-9dad-4958-bab6-f913486cd377" />



### 2. Hybrid Model (SDXL + Real Objects)
*Trained on a combination of synthetic scenes and real-world object photos from Roboflow.*

| Confusion Matrix (Hybrid) | Training Curves (Hybrid) |
| :---: | :---: |
|<img width="932" height="699" alt="image" src="https://github.com/user-attachments/assets/f91989f8-93ab-41fb-adf6-f99a0fa188b4" />|<img width="1109" height="481" alt="image" src="https://github.com/user-attachments/assets/562f9996-065c-4558-aae9-9e78d48d72fa" /> |

| Output examples for individual objects | Output examples for room |
| :---: | :---: |
<img width="1350" height="1350" alt="image" src="https://github.com/user-attachments/assets/bdf597f8-707d-493d-af3b-e17d4cb1f96a" /> | <img width="790" height="812" alt="Без названия (4)" src="https://github.com/user-attachments/assets/606d482c-255d-4291-97b8-aa64001e6ba6" />


| Metric | Synthetic-Only Model | Hybrid Model (Final) |
| :--- | :---: | :---: |
| **mAP50** | 0.40 | **0.90** |
| **F1-Score** | 0.39 | **0.90** |

**Conclusion:**
• AI-based computer vision can effectively detect hazards in children’s rooms

• Synthetic data helps address privacy and ethical concerns, but works best when combined with real data

• Hybrid models significantly improve detection accuracy and reduce false positives

• Separating object detection from hazard classification creates a modular and explainable system

• The proposed solution has strong potential for real-world use in smart homes and child safety systems



---

## 📂 Repository Structure
* **`01_generate_images.ipynb`**: SDXL-based room generation pipeline.
* **`Creating and marking individual...`**: Object isolation and auto-labeling for only syntetic train.
* **`only_syntetic_train_yolo.ipynb`**: Baseline YOLO training.
* **`hybrid_model.ipynb`**: Advanced training with mixed datasets.
* **`First/Second/Third Presentation.pptx`**: Interim reports on the development progress.
* **`Final Presentation.pptx`**: Comprehensive project summary.
