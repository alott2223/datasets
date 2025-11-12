# COCO (Common Objects in Context)

## Overview
COCO is a large-scale object detection, segmentation, and captioning dataset. It contains photos of 91 object types with a total of 2.5 million labeled instances across 328,000 images.

## Specifications
- **Size**: ~25 GB (2017 version)
- **Format**: JPEG images with JSON annotations
- **License**: Creative Commons Attribution 4.0
- **Resolution**: Variable (resized to specific dimensions for tasks)
- **Domain**: Everyday objects in natural contexts

## Source
- Official website: [https://cocodataset.org/](https://cocodataset.org/)
- Download: [https://cocodataset.org/#download](https://cocodataset.org/#download)
- Paper: [https://arxiv.org/abs/1405.0312](https://arxiv.org/abs/1405.0312)
- GitHub: [https://github.com/cocodataset/cocoapi](https://github.com/cocodataset/cocoapi)

## Statistics (2017 version)
- **Images**: 
  - Train: 118K images
  - Validation: 5K images
  - Test: 41K images
- **Object Categories**: 80 classes (91 including stuff)
- **Instance Annotations**: 2.5M instances
- **Captions**: 5 captions per image

### Tasks Supported:
1. **Object Detection**: Bounding box detection
2. **Instance Segmentation**: Pixel-level instance masks
3. **Keypoint Detection**: Person keypoint estimation
4. **Panoptic Segmentation**: Unified segmentation
5. **Image Captioning**: Natural language descriptions
6. **Dense Pose**: Human pose estimation

### Object Categories:
- Person, bicycle, car, motorcycle, airplane, bus, train, truck, boat
- Traffic light, fire hydrant, stop sign, parking meter, bench
- Bird, cat, dog, horse, sheep, cow, elephant, bear, zebra, giraffe
- Backpack, umbrella, handbag, tie, suitcase
- Frisbee, skis, snowboard, sports ball, kite, baseball bat
- And 55 more categories...

## Usage

### Using pycocotools
```python
from pycocotools.coco import COCO
import matplotlib.pyplot as plt
from PIL import Image

# Load annotations
dataDir = '/path/to/coco'
dataType = 'train2017'
annFile = f'{dataDir}/annotations/instances_{dataType}.json'

coco = COCO(annFile)

# Get all images containing a specific category
catIds = coco.getCatIds(catNms=['person'])
imgIds = coco.getImgIds(catIds=catIds)
img = coco.loadImgs(imgIds[0])[0]

# Load and display image
I = Image.open(f"{dataDir}/{dataType}/{img['file_name']}")
plt.imshow(I)
plt.show()

# Load annotations
annIds = coco.getAnnIds(imgIds=img['id'], catIds=catIds)
anns = coco.loadAnns(annIds)
coco.showAnns(anns)
```

### Using PyTorch
```python
from torchvision.datasets import CocoDetection
import torchvision.transforms as transforms

# Define transforms
transform = transforms.Compose([
    transforms.Resize((224, 224)),
    transforms.ToTensor(),
])

# Load dataset
train_dataset = CocoDetection(
    root='/path/to/coco/train2017',
    annFile='/path/to/coco/annotations/instances_train2017.json',
    transform=transform
)
```

### Using TensorFlow
```python
import tensorflow_datasets as tfds

# Load dataset
ds_train = tfds.load('coco/2017', split='train')
ds_val = tfds.load('coco/2017', split='validation')

for example in ds_train.take(1):
    image = example['image']
    objects = example['objects']
    print(f"Image shape: {image.shape}")
    print(f"Objects: {objects}")
```

### Annotation Format (JSON)
```json
{
  "images": [
    {
      "id": 397133,
      "file_name": "000000397133.jpg",
      "height": 427,
      "width": 640
    }
  ],
  "annotations": [
    {
      "id": 1768,
      "image_id": 397133,
      "category_id": 1,
      "bbox": [199, 200, 100, 150],
      "area": 15000,
      "segmentation": [[...]],
      "iscrowd": 0
    }
  ],
  "categories": [
    {
      "id": 1,
      "name": "person",
      "supercategory": "person"
    }
  ]
}
```

## Citation
```bibtex
@inproceedings{lin2014microsoft,
  title={Microsoft coco: Common objects in context},
  author={Lin, Tsung-Yi and Maire, Michael and Belongie, Serge and Hays, James and Perona, Pietro and Ramanan, Deva and Doll{\'a}r, Piotr and Zitnick, C Lawrence},
  booktitle={European conference on computer vision},
  pages={740--755},
  year={2014},
  organization={Springer}
}
```

## Notes
- COCO is one of the most widely used benchmarks for object detection
- Images feature objects in natural contexts with complex scenes
- Provides rich annotations including bounding boxes, segmentation masks, and keypoints
- Annual COCO challenges drive innovation in computer vision
- The dataset is well-maintained with clear documentation
- Available through multiple interfaces (pycocotools, TensorFlow, PyTorch)
- Consider using the COCO API for efficient data loading and evaluation
- The 2017 version is the most commonly used
- Be aware that some images may contain people - consider privacy implications
- The dataset is relatively balanced but some categories have more instances than others
