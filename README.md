# FloodNet UAV Flood Segmentation

## Objective
Semantic segmentation of UAV aerial images to detect flooded and non-flooded regions using the FloodNet dataset.

## Dataset
- **Dataset:** [FloodNet Track-1 on Kaggle](https://www.kaggle.com/datasets/aletbm/aerial-imagery-dataset-floodnet-challenge)
- 10 semantic classes (Background, Buildings, Roads, Water, Vegetation, etc.)
- ~398 labeled UAV images with corresponding segmentation masks
- High-resolution aerial data (3000–4500 px), resized to 256x256 for efficient training

## Work Completed
1. Dataset exploration and verification of image–mask alignment  
2. Analysis of class distribution and handling of imbalance  
3. Preprocessing (resizing, normalization, tensor conversion)  
4. Basic data augmentation (horizontal and vertical flips)  
5. Exported preprocessed and augmented data to `../data/Processed/`  
6. Created fixed color palette for semantic classes for consistent visualization  

## Planned Pipeline
1. Implement PyTorch `Dataset` and `DataLoader` for preprocessed data  
2. Define UNet architecture for multi-class segmentation  
3. Configure weighted CrossEntropy loss and optimizer (Adam)  
4. Train and validate model on processed FloodNet data  
5. Evaluate performance using IoU and Dice score  
6. Visualize predictions using fixed class color mapping  

## Environment
- Python 3.x  
- PyTorch (MPS backend for Apple Silicon)  
- torchvision  
- numpy  
- matplotlib  
- pillow  
- scikit-learn  

## Next Steps
- Implement training and validation loops  
- Compare UNet with baseline CNN segmentation models  
- Evaluate on unseen UAV flood scenes