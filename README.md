# Hedgehog Sanctuary RGB-Thermal Dataset

## Overview
This dataset consists of **1,762 paired RGB and thermal images** collected from a **hedgehog sanctuary (Igelauffangstation)**. It is designed for research on thermal and RGB vision tasks, particularly for hedgehog detection and related applications.

## Dataset Structure
The dataset is organized into the following folders:

### Raw Data
- **`olive_cam_synchronized/`**  
  *Raw dataset from the RGB camera.*

- **`thermal_synchronized/`**  
  *Raw thermal dataset from the Optris PI640i.*

### Data Split into Train/Val/Test Folders for Training
- **`rgb/`**  
  *RGB images extracted from `olive_cam_synchronized` and split into `train`, `val`, and `test` folders.*

- **`thermal/`**  
  *Thermal images in TIFF format, also split into `train`, `val`, and `test` folders.*

- **`thermal_8bit/`**  
  *8-bit JPG thermal images for easier processing, similarly split into `train`, `val`, and `test` folders.*

### Annotations
- **`annotations/`**  
  *Contains COCO-style annotations for both the RGB and thermal datasets.*

### YOLO Dataset Splits
These folders contain images and labels formatted for training with YOLO:
- **`rgb_yolo/`**  
  *RGB dataset with YOLO-style labels, structured into `/images` and `/labels` subfolders.*
- **`thermal_8bit_yolo/`**  
  *8-bit thermal dataset with YOLO-style labels, also structured into `/images` and `/labels`.*

### Synthetic Data
- **`fake_thermal/`**  
  *RGB images adapted to resemble the thermal domain, intended for domain adaptation experiments.*

## Dataset Limitations
While the dataset provides a diverse range of thermal and RGB images, it has some limitations that should be considered when applying models trained on it to real-world scenarios:

- **Indoor environment:**  
  The dataset was recorded exclusively indoors, which does not fully represent outdoor conditions where a mowing robot would typically operate.

- **Lack of natural elements:**  
  The dataset does not include natural elements such as grass, soil, or foliage, which could introduce additional detection challenges.

- **Limited occlusions:**  
  In real gardens, occlusions from grass, leaves, or other obstacles are frequent. The dataset contains fewer occlusions, potentially making detection easier than in outdoor environments.

- **Environmental differences:**  
  Outdoor conditions involve temperature fluctuations, wind, and varying lighting, which are absent in this dataset and may affect model generalization.

## Usage
This dataset can be used for tasks such as:
- Object detection in thermal and RGB images.
- Multi-modal image analysis and sensor fusion.
- Hedgehog and small animal detection in controlled environments.

## Citation
If you use this dataset in your research, please cite it as follows:
```bibtex
@misc{hedgehog_thermal_dataset,
  title={Hedgehog Sanctuary RGB-Thermal Dataset},
  author={Your Name},
  year={2025},
  note={Available at https://github.com/YOUR_REPO}
}
```
## License
This dataset is available under the [Creative Commons Attribution 4.0 International (CC BY 4.0) License](https://creativecommons.org/licenses/by/4.0/).
You are free to share and adapt the material for any purpose, even commercially, as long as you provide proper attribution.

