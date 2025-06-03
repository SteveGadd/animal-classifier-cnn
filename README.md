# Animal Image Classifier

A Convolutional Neural Network (CNN) built from scratch using PyTorch to classify images across 90 different animal species.

## 📊 Results

- **Accuracy:** 95.00%
- **Training Time:** 15 minutes (10 epochs)
- **Dataset Size:** 5,400 images across 90 classes (~60 images per class)

## 🗂️ Dataset

This project uses the [Animal Image Dataset (90 Different Animals)](https://www.kaggle.com/datasets/iamsouravbanerjee/animal-image-dataset-90-different-animals) from Kaggle, featuring diverse animal species from around the world.

**Dataset Statistics:**
- 90 unique animal classes
- 5,400 total images
- Images automatically downloaded via `kagglehub`

## 🏗️ Model Architecture

Custom CNN with the following structure:
```
Input (3, 224, 224) 
    ↓
Conv2d(3→32) + ReLU + MaxPool2d
    ↓  
Conv2d(32→64) + ReLU + MaxPool2d
    ↓
Conv2d(64→64) + ReLU + MaxPool2d
    ↓
Flatten + Linear(64*26*26 → 90)
```

**Key Features:**
- Progressive feature learning (edges → shapes → complex patterns)
- Pooling layers to reduce computational complexity
- 90 output classes for final classification

### Training Details

- **Optimizer:** Adam (lr=1e-3)
- **Loss Function:** CrossEntropyLoss
- **Batch Size:** 32
- **Image Size:** 224x224 pixels
- **Data Split:** 80% train, 20% validation
- **Random Seed:** 1864 (for reproducible results)

## 📈 Training Progress

The model showed steady improvement across epochs:
```
Epoch 0: Loss ~4.5 → Epoch 9: Loss ~0.5-0.8
Final Validation Accuracy: 95.00%
```

## 🔍 Key Learning Outcomes

This project demonstrates:
- CNN architecture design for image classification
- Working with real-world datasets using kagglehub
- PyTorch fundamentals (DataLoader, transforms, training loops)
- Achieving strong performance with limited data (60 images/class)

## 💻 View Results

🔗 **[View Live Notebook with Outputs](https://colab.research.google.com/drive/1P2PFeypuTVNDolRn7aEAevA5Dj-aVnrj?usp=sharing)**

*Click the link above to see the complete notebook with training outputs, visualizations, and results without needing to run the code.*

## 📄 License

This project is open source and available under the MIT License.
