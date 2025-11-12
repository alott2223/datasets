# ImageNet

## Overview
ImageNet is a large-scale visual database designed for use in visual object recognition research. It contains over 14 million images organized according to the WordNet hierarchy.

## Specifications
- **Size**: ~150 GB (ILSVRC2012 subset)
- **Format**: JPEG images
- **License**: Research and educational use (registration required)
- **Resolution**: Variable (typically resized to 256x256 or 224x224)
- **Domain**: General object recognition

## Source
- Official website: [https://www.image-net.org/](https://www.image-net.org/)
- Download: [https://www.image-net.org/download.php](https://www.image-net.org/download.php) (registration required)
- Paper: [https://ieeexplore.ieee.org/document/5206848](https://ieeexplore.ieee.org/document/5206848)

## Statistics
- **Total Images**: 14+ million images
- **Synsets**: 21,841 WordNet synsets
- **ILSVRC2012 Classification**: 
  - Training: 1.2M images
  - Validation: 50K images
  - Test: 100K images
  - Classes: 1,000 categories

### Class Examples:
- Animals (mammals, birds, fish, reptiles, insects)
- Vehicles (cars, planes, boats)
- Household objects (furniture, appliances)
- Plants and food
- Natural objects

## Usage

### Using PyTorch
```python
from torchvision import datasets, transforms

# Define transforms
transform = transforms.Compose([
    transforms.Resize(256),
    transforms.CenterCrop(224),
    transforms.ToTensor(),
    transforms.Normalize(mean=[0.485, 0.456, 0.406],
                       std=[0.229, 0.224, 0.225])
])

# Load dataset
train_dataset = datasets.ImageNet(
    root='/path/to/imagenet',
    split='train',
    transform=transform
)

val_dataset = datasets.ImageNet(
    root='/path/to/imagenet',
    split='val',
    transform=transform
)
```

### Using TensorFlow
```python
import tensorflow as tf
import tensorflow_datasets as tfds

# Load dataset
train_ds = tfds.load('imagenet2012', split='train', as_supervised=True)
val_ds = tfds.load('imagenet2012', split='validation', as_supervised=True)

# Preprocess
def preprocess(image, label):
    image = tf.image.resize(image, [224, 224])
    image = tf.cast(image, tf.float32) / 255.0
    return image, label

train_ds = train_ds.map(preprocess).batch(32)
```

### Directory Structure
```
imagenet/
├── train/
│   ├── n01440764/  (class folder)
│   │   ├── n01440764_10026.JPEG
│   │   ├── n01440764_10027.JPEG
│   │   └── ...
│   ├── n01443537/
│   └── ...
└── val/
    ├── n01440764/
    └── ...
```

## Citation
```bibtex
@inproceedings{deng2009imagenet,
  title={Imagenet: A large-scale hierarchical image database},
  author={Deng, Jia and Dong, Wei and Socher, Richard and Li, Li-Jia and Li, Kai and Fei-Fei, Li},
  booktitle={2009 IEEE conference on computer vision and pattern recognition},
  pages={248--255},
  year={2009},
  organization={IEEE}
}
```

## Notes
- ImageNet is the foundation of the annual ImageNet Large Scale Visual Recognition Challenge (ILSVRC)
- Most popular pre-trained models are trained on ImageNet
- Standard benchmark for image classification
- Registration and agreement to terms of use required for download
- The dataset has been influential in advancing computer vision research
- Consider ethical implications: the dataset has been critiqued for labeling issues and bias
- Some categories have been deprecated due to offensive labels
- Images are sourced from the web and may have varying quality
- Pre-trained weights on ImageNet are widely available (ResNet, VGG, Inception, etc.)
