## README.md

# 🐜 Insect Classification AI (ImageNet Transfer Learning)
A production-ready deep learning pipeline that leverages an ImageNet-pretrained backbone to classify insect images into specific entomological categories.

---## 🛠️ Project Architecture

├── data/ # Local evaluation and training data
├── models/ # Model checkpoints and architecture definitions
├── utils/ # Image preprocessing and post-processing tools
├── classify.py # Main CLI script for single/batch inference
├── requirements.txt # Python dependencies
└── README.md # Project documentation


### Technical Workflow
1. **Preprocessing**: Input images are automatically resized to `224x224` pixels, normalized to ImageNet statistics (`mean=[0.485, 0.456, 0.406]`, `std=[0.229, 0.224, 0.225]`), and converted to tensors.
2. **Feature Extraction**: A MobileNetV3/ResNet50 backbone (pretrained on ImageNet) extracts low-level and high-level visual features.
3. **Classification Head**: Custom fully connected layers map the extracted features into precise insect classes using a Softmax activation.


