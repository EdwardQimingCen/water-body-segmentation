# Water Body Segmentation

Automatic water body detection in remote sensing imagery using U-Net + ResNet34.

## Project Overview

Have you ever wondered how scientists monitor water bodies like rivers, lakes, and ponds from space? This project tackles exactly that challenge using the power of deep learning and satellite imagery.

We've built a smart system that can automatically identify and map water bodies in satellite images. Think of it as teaching a computer to "see" water the same way humans do, but much faster and more consistently. The system takes satellite images as input and produces precise maps showing exactly where water is located.

**Why is this important?**
- **Environmental Monitoring**: Track changes in water bodies over time to understand environmental impacts
- **Disaster Response**: Quickly assess flood extent during natural disasters to help emergency responders
- **Water Resource Management**: Monitor water availability for agriculture, urban planning, and conservation efforts
- **Climate Research**: Study how water bodies change due to climate variations and human activities

**What makes our approach special?**
We use a combination of two powerful technologies: U-Net (great at image segmentation) and ResNet34 (excellent at understanding image features). This combination gives us the best of both worlds - accuracy and efficiency. Our model achieves over 70% IoU score, which means it correctly identifies water bodies with high precision.

The whole system is designed to be practical and accessible. You can run it on a regular computer with a GPU, and it processes images quickly enough for real-world applications.

## Performance

```
IoU: 70.3%
Dice: 82.6%
Accuracy: 89.4%
```

## Model

- **Architecture**: U-Net + ResNet34 encoder
- **Input**: 256×256 RGB images
- **Output**: Binary segmentation masks (water/background)
- **Parameters**: 24.4M
- **Model Size**: 93.2 MB

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

- **Epochs**: 30
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



