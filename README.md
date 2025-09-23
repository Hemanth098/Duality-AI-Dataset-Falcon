# 🚨 Duality AI Detection with YOLOv8

This project trains a YOLOv8 object detection model to identify **safety equipment** in space environments.  
The model is capable of detecting **7 classes** of objects:  

- 🟢 OxygenTank  
- 🔵 NitrogenTank  
- 🩹 FirstAidBox  
- 🔔 FireAlarm  
- ⚡ SafetySwitchPanel  
- ☎️ EmergencyPhone  
- 🔴 FireExtinguisher  

---

## 📂 Dataset
The dataset is custom-built and organized in YOLO format:  

```yaml
train: Training_folder
val: validation_folder
test: testing_folder
nc: 7
names: ['OxygenTank', 'NitrogenTank', 'FirstAidBox', 'FireAlarm', 'SafetySwitchPanel', 'EmergencyPhone', 'FireExtinguisher']
```
##🚀 Inference

Run inference on an image:

yolo detect predict \
  model=runs/detect/train/weights/best.pt \
  source=path/to/image.jpg \
  conf=0.5


Predictions will be saved in runs/detect/predict/.


## 🧪 Example Predictions

### First Aid Box
![FirstAid Prediction](https://github.com/Hemanth098/Duality-AI-Dataset-Falcon/blob/main/runs/detect/predict/000000031_dark_clutter.jpg)

### Fire Extinguisher
![FireExtinguisher Prediction](https://github.com/Hemanth098/Duality-AI-Dataset-Falcon/blob/main/runs/detect/predict2/000000008_vlight_unclutter.jpg)

### Oxygen Tank
![OxygenTank Prediction](https://github.com/Hemanth098/Duality-AI-Dataset-Falcon/blob/main/runs/detect/predict3/000000008_vlight_unclutter.jpg)
