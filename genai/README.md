# little-gem: Mixture of Experts Multimodal Toy Model

This repository contains a Jupyter notebook demonstrating a simple **Mixture of Experts** neural network model combining text and image modalities for animal and sound recognition. Inspired by Google's Gemini architecture, this educational "little-gem" project illustrates fundamental multimodal fusion concepts with easy-to-understand TensorFlow/Keras code.

## Features
- Combines text (using Universal Sentence Encoder) and image (MobileNetV2) experts
- Mixture of Experts gating to decide modality influence
- Custom Keras layers for gating, padding, and softmax temperature scaling
- Data loaders for cats vs dogs dataset and synthetic text inputs
- Training and evaluation pipeline with detailed explanations

## Requirements
- Python 3.10.17
- TensorFlow 2.19.1 and associated libraries
- numpy, requests, Pillow for image processing and networking

Install dependencies using:

```
pip install -r requirements.txt
```


## Usage
1. Open the notebook in Jupyter or Colab
2. Follow along with the step-by-step explanations and code cells
3. Train the model on combined multimodal data
4. Run inference examples on text-only, image-only, or multimodal inputs
5. Modify and extend the notebook for further experimentation

## Disclaimer
The real Gemini AI architecture is highly sophisticated and optimized beyond this toy example. This notebook serves purely as an educational starting point to explore how mixture of experts and multimodality ideas can be implemented from scratch.

---

Created by Himal Dwarakanath | GenAI Enthusiast  
Feel free to explore, adapt, and contribute!