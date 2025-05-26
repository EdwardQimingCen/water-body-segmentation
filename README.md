# AI4EO Water Body Segmentation

Automatic water body detection in remote sensing imagery using U-Net + ResNet34.

## 🎯 Project Overview

This project uses deep learning to automatically detect water bodies (rivers, lakes, ponds) in satellite images for environmental monitoring and water resource management.

## 📊 Performance

```
IoU: 70.3%
Dice: 82.6%
Accuracy: 89.4%
```

## 🏗️ Model

- **Architecture**: U-Net + ResNet34 encoder
- **Input**: 256×256 RGB images
- **Output**: Binary segmentation masks (water/background)
- **Parameters**: 24.4M
- **Model Size**: 93.2 MB

## 📁 Structure

```
project/
├── data/
│   ├── images/     # Input images
│   └── masks/      # Ground truth masks
├── models/         # Saved models
├── segmentation.ipynb # Main code
└── README.md
```

## 🚀 Quick Start

1. Install dependencies: `pip install -r requirements.txt`
2. Place data in `data/` folder
3. Run `segmentation.ipynb`

## 🛠️ Training Details

- **Epochs**: 30
- **Batch Size**: 16
- **Learning Rate**: 0.0003
- **Loss**: Dice + BCE
- **Data Split**: 70% train, 15% val, 15% test

## 🌍 Environmental Impact

- **GPU Usage**: CUDA enabled
- **Benefits**: Automated water monitoring, flood assessment, resource management

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📚 References

1. **U-Net Architecture**  
   Ronneberger, O., Fischer, P., & Brox, T. (2015). U-Net: Convolutional Networks for Biomedical Image Segmentation. *Medical Image Computing and Computer-Assisted Intervention*, 234-241.  
   [Paper](https://arxiv.org/abs/1505.04597)

2. **ResNet Architecture**  
   He, K., Zhang, X., Ren, S., & Sun, J. (2016). Deep Residual Learning for Image Recognition. *IEEE Conference on Computer Vision and Pattern Recognition*, 770-778.  
   [Paper](https://arxiv.org/abs/1512.03385)


## 🔗 Useful Resources

- [PyTorch Documentation](https://pytorch.org/docs/)
- [Earth Observation Data](https://earthexplorer.usgs.gov/)

## 📞 Contact

[Edward Cen] - [edwardcen51@gmail.com]

---

*AI for Earth Observation - Water Resource Monitoring*



