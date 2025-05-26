# Water Body Segmentation

This project implements an automated water body detection system using deep learning and satellite imagery. Using a custom CNN with U-Net decoder architecture, the system can automatically identify and map water bodies in satellite images, producing precise segmentation maps for environmental monitoring and disaster response applications.

## Project Overview

Have you ever wondered how scientists monitor water bodies like rivers, lakes, and ponds from space? This project tackles exactly that challenge using the power of deep learning and satellite imagery.

I've built a model that can automatically identify and map water bodies in satellite images. The system takes satellite images as input and produces precise maps showing exactly where water is located.

**Why is this important?**
- **Environmental Monitoring**: Track changes in water bodies over time to understand environmental impacts
- **Disaster Response**: Quickly assess flood extent during natural disasters to help emergency responders
- **Water Resource Management**: Monitor water availability for agriculture, urban planning, and conservation efforts
- **Climate Research**: Study how water bodies change due to climate variations and human activities

**What makes my approach special?**
I use a custom CNN with U-Net decoder architecture that combines powerful feature extraction with precise segmentation capabilities. This hybrid approach gives me the best of both worlds - accuracy and efficiency. My model achieves 62.5% IoU score with 76.9% Dice coefficient, which means it correctly identifies water bodies with good precision while maintaining computational efficiency.

The whole system is designed to be practical and accessible. You can run it on a regular computer with a GPU, and it processes images quickly enough for real-world applications with early stopping at just 16 epochs.

## Dataset

This project uses the **Satellite Images of Water Bodies** dataset from Kaggle.

**Source:** [Satellite Images of Water Bodies](https://www.kaggle.com/datasets/franciscoescobar/satellite-images-of-water-bodies)

**Description:**
- Sentinel-2 satellite imagery with binary water masks
- Images: 256×256 RGB format
- Masks: Black and white (white = water, black = background)
- Generated using NDWI (Normalized Difference Water Index)

**Statistics:**
- Total pixels: 27,983,872
- Water: 27.6%, Background: 72.4%

## Model Performance

- **IoU Score**: 0.625
- **Dice Coefficient**: 0.769  
- **Pixel Accuracy**: 0.875
- **Recall**: 0.754 (Critical for disaster monitoring)

## Architecture

Custom CNN with U-Net decoder  
Total parameters: 3,869,857  
Model size: 14.8 MB  
Actual training epochs: 16

## Structure

```
project/
├── data/
│   ├── images/     # Input images
│   └── masks/      # Ground truth masks
├── models/         # Saved models
├── segmentation.ipynb # Main code
└── README.md
```

## Quick Start

1. Install dependencies: `pip install -r requirements.txt`
2. Place data in `data/` folder
3. Run `segmentation.ipynb`

## Training Details

- **Epochs**: 40
- **Batch Size**: 16
- **Learning Rate**: 0.0003
- **Loss**: Dice + BCE
- **Data Split**: 70% train, 15% val, 15% test

## Environmental Impact

- **GPU Usage**: CUDA enabled
- **Benefits**: Automated water monitoring, flood assessment, resource management

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


## Contact

[Edward Cen] - [edwardcen51@gmail.com]

---



