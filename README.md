# FloodNet UAV Flood Segmentation

## Objective
Semantic segmentation of UAV aerial images to detect flooded and non-flooded regions using the FloodNet dataset.

## Dataset
- **Dataset:** [FloodNet Track-1 on Kaggle](https://www.kaggle.com/datasets/aletbm/aerial-imagery-dataset-floodnet-challenge)
- 10 semantic classes (Background, Buildings, Roads, Water, Vegetation, etc.)
- ~398 labeled UAV images with corresponding segmentation masks
- High-resolution aerial data (3000–4500 px), resized to 512x512 patches to preserve spatial details
- Dataset split ensured no overlap between train, validation, and test sets at the parent image level
- Class imbalance handled through computed class-frequency weights stored in a JSON file

## Work Completed
1. Dataset exploration and verification of image–mask alignment  
2. Analysis of class distribution and computation of class-frequency-based weights  
3. Preprocessing (resizing, normalization, tensor conversion)  
4. Data augmentation (horizontal and vertical flips)  
5. Exported preprocessed and augmented data to `../data/Processed_v3/`  
6. Implemented uniform tiling and parent-based data splitting for fair evaluation  
7. Integrated weighted CrossEntropy loss to address class imbalance  
8. Developed UNet architecture with ResNet34 encoder for multi-class segmentation  
9. Implemented stable training and validation loops with checkpoint saving  
10. Validated on unseen test data to evaluate generalization and per-class IoU performance  
11. Visualized qualitative results with random prediction overlays for comparison  

## Planned Pipeline
1. Implement PyTorch `Dataset` and `DataLoader` for preprocessed data  
2. Define UNet architecture for multi-class segmentation  
3. Configure weighted CrossEntropy loss and optimizer (Adam)  
4. Train and validate model on processed FloodNet data  
5. Evaluate performance using IoU and Dice score  
6. Visualize predictions using fixed class color mapping  
7. Evaluate trained model on unseen UAV flood test data  
8. Document per-class IoU and mIoU for result comparison and reporting  

## Environment
- Python 3.x  
- PyTorch  
- torchvision  
- numpy  
- matplotlib  
- pillow  
- scikit-learn  
- albumentations  

## Future Steps
- Compare UNet with deeper encoder backbones for feature enrichment  
- Evaluate and refine model on additional unseen UAV flood data  
- Investigate model performance improvements through fine-tuning and loss adjustments  
- Explore advanced segmentation architectures such as DeepLabV3+ and Attention UNet  