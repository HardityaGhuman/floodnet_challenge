# FloodNet UAV Flood Segmentation

## Objective
Semantic segmentation of UAV aerial images to detect flooded and non-flooded regions.

## Dataset
FloodNet (Track-1)  
10 semantic classes  
~398 labeled images, high-resolution UAV footage
Dataset: [FloodNet Track-1 on Kaggle](https://www.kaggle.com/datasets/aletbm/aerial-imagery-dataset-floodnet-challenge)

## Pipeline
1. Data understanding
2. Preprocessing & augmentation
3. Train/validation split
4. UNet model training
5. Evaluation (IoU, Dice)
6. Results visualization

## Environment
- Python 3.x
- PyTorch (MPS for Apple Silicon)

## Next Steps
- Implement training loops
- Compare UNet with baseline
- Evaluate on unseen flood scenes