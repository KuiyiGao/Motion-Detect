# Object Momentum Classification Using Semantic Segmentation DNNs
May 2025, ELEG5491 Project
## Motivation
This project introduces a fast Deep Neural Network for semantic classification for different levels of momemtum of objects. This network will
provide a quick insight for autonomous systems on "where to focus" within the field of view and mitigate the risk of collision.
## 🚀Features
- Dataset: Utilizing COCO-stuff dataset and remapped the annotations to four levels of momemtum.
- Network: Simplified DeepLab-V3-Resnet-50 with reduced ASPP head, reducing training and inference cost by 20%
- Performance: weighted cross entropy loss and IoU scores for training, optimal loss of 0.75 and optimal IoU of 0.6, realized a 58 FPS inference speed on NVIDIA GTX4090, proven potential to
- deploy on computing devices such as NVIDIA Jetson Nano
## 💻Project Structure
.
├── dataset/
│   ├── train/          # COCO-Stuff images/annotations
│   ├── val/            # Validation set
│   └── lut.npy         # Momentum mapping LUT configuration
├── src/
│   ├── model.py        # Modified DeepLabV3 with simplified ASPP
│   ├── dataset.py      # Custom dataset & transform logic
│   ├── train.py        # Training & validation loop
│   └── create_lut.py   # Mapping logic from COCO labels to Momentum
└── README.md

## Youtube Demo: https://www.youtube.com/watch?v=oluNSNQs7zY
## Acknowledgement: 
Thanks for the amazing lectures by Prof. Hongsheng Li and the help provided by his Ph.D students.
