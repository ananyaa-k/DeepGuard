# DeepGuard: Adversarial Deepfake Detection Pipeline 👁️

**DeepGuard** is a real-time deepfake detection framework designed to identify synthetic media manipulation in video streams. 

Unlike standard detection models that focus solely on accuracy, DeepGuard prioritizes **Model Robustness**. It employs **Adversarial Training** (using the Fast Gradient Sign Method - FGSM) to harden the detection engine against evasion attacks and noise-based bypass attempts.

## 🔬 Research Focus
Standard CNNs (like Xception or MesoNet) are often brittle; slight pixel perturbations can cause them to misclassify a deepfake as "Real." DeepGuard aims to solve this by:
1.  **Ingestion:** Real-time frame extraction using **OpenCV**.
2.  **Detection:** Utilizing a custom-tuned **MesoNet** architecture for detecting face swapping/reenactment.
3.  **Defense:** Integrating an **Adversarial Defense Loop** where the model is iteratively trained on perturbed examples to resist evasion.

## 🛠️ Tech Stack
* **Core Logic:** Python 3.9
* **Deep Learning:** TensorFlow / Keras
* **Computer Vision:** OpenCV (Haar Cascades / MTCNN)
* **Adversarial Libs:** CleverHans / ART (Adversarial Robustness Toolbox)
* **Deployment:** Docker & FastAPI

## 📅 Implementation Roadmap
- [x] Literature Review & Architecture Design
- [ ] Pipeline Setup (Video Ingestion)
- [ ] Baseline Model Training (MesoNet on FaceForensics++)
- [ ] Adversarial Attack Simulation (FGSM Generation)
- [ ] Robustness Evaluation & Retraining

*This project is part of an ongoing research initiative into AI Safety and Media Forensics.*
