# IntoxDetect

![License](https://img.shields.io/badge/license-GPL--3.0-blue.svg)

## Overview

IntoxDetect is a research project that leverages computer vision and deep learning to detect signs of intoxication through facial analysis. The system employs multiple CNN architectures to analyze both facial features and pupil dilation patterns, providing a comprehensive approach to intoxication detection. Full paper published in IEEE Xplore: https://ieeexplore.ieee.org/document/10900115

## Project Structure

```
IntoxDetect/
├── models/
│   ├── face_detection/
│   │   ├── inception_resnet_v2/
│   │   └── vgg16/
│   └── pupil_dilation/
│       ├── inception_resnet_v2/
│       └── vgg16/
├── preprocessing/
│   ├── face_cropping/
│   └── eye_detection/
├── notebooks/
│   ├── face_detection/
│   ├── pupil_dilation/
│   └── preprocessing/
├── data/
│   ├── face_dataset/
│   └── eye_dataset/
├── requirements.txt
├── LICENSE
└── README.md
```

## Features

- **Face Detection Models**
  - Inception-ResNet-V2 based CNN
  - VGG16 based CNN
  - Binary classification (drunk/sober)

- **Pupil Dilation Analysis**
  - Inception-ResNet-V2 based CNN
  - VGG16 based CNN
  - Multi-class classification (forward/left/right/closed)

- **Preprocessing Pipeline**
  - YOLO-based face detection and cropping
  - Eye region detection and extraction
  - Standardized image preprocessing

## Datasets

1. **RoboFlow Face Dataset**
   - 2,468 total images
   - Binary classification: "drunk" vs "sober"
   - Used for face-based intoxication detection

2. **Kaggle Eye Direction Dataset**
   - 14,500 total images
   - Multi-class classification: "forward", "left", "right", "closed"
   - Used for pupil dilation analysis

## Getting Started

### Prerequisites

- Python 3.8+
- CUDA-capable GPU (recommended)
- Google Colab account (for running notebooks)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/ShauryaVM/IntoxDetect.git
   cd IntoxDetect
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Usage

1. **Running the Models**
   - Open the desired notebook in Google Colab
   - Enable GPU runtime (Runtime > Change runtime type > GPU)
   - Follow the notebook instructions for dataset upload and model training

2. **Preprocessing Pipeline**
   - Use the preprocessing notebooks to prepare your data
   - Follow the specified data organization structure

## Model Performance

- Results may vary due to:
  - Random weight initialization
  - Data shuffling
  - Hardware differences
- For consistent results, use the same hardware and seed settings

## Contributing

This is a research project. If you wish to contribute:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- 2024 4th International Conference on Artificial Intelligence, Robotics, and Communication (ICAIRC) for publication of our results
- RoboFlow for the face dataset
- Kaggle for the eye direction dataset

## Abstract

Every day, nearly 37 people in the United States die in drunk-driving crashes—one person every 39 minutes. Despite significant progress in reducing drunk driving over the past decades, recent years have seen a troubling rise in alcohol-related accidents. Present methods of assessing intoxication are expensive, time-consuming, and often require specialized equipment and trained personnel(Sevincer2014). Traditional breathalyzers, blood tests, and field sobriety tests, while effective, are not always practical for widespread and routine use. As a result, non-invasive methods to detect intoxication so that drinkers can be warned proactively, are desirable. We propose a novel method of detecting intoxication through facial image analysis that can be used to combat drunk driving. We benchmarked the performance of GPT-4o as a classifier compared to CNN architectures on the face and eye image data. We found that the VGG16 and the Inception-ResNet-V2 models, trained & fine-tuned on 10000 facial images, had high accuracies of 83% and 82%, respectively, in detecting inebriation on the test sets. Considering there are no other variables besides the images, the model has immense potential as an AI facial intoxication detection system.

## Contact

For questions or collaboration opportunities, please open an issue in the repository.

Authors: Shaurya Mantrala, Idhant Gode, Devang Pandey, Swayam Shah
