# CVIP360_BBox_Annotations
## Overview
This repository contains custom bounding box annotations derived from the **CVIP360 dataset**: https://drive.google.com/drive/folders/1LMPW3HJHtqMGcIFXFo74x3t0Kh2REuoS
, which was originally released for **depth estimation** in omni-directional imaging. The CVIP360 dataset provides high-resolution 360° equirectangular frames with rich geometric structure, making it a strong baseline for omni-directional scene understanding.

To enable research in **360-degree object detection**, this project adds new **YOLO-format bounding box annotations** on top of the original CVIP360 dataset. These annotations are designed to be compatible with wrap-around, projection-aware detection pipelines, including models modified for spherical or equirectangular vision.


---

## Dataset Structure
The folder structure follows standard YOLO layout:

```
dataset/
 ├── train/
 │    ├── images/
 │    └── labels/
 ├── valid/
 │    ├── images/
 │    └── labels/
 ├── test/
 │    ├── images/
 │    └── labels/
 ├── data.yaml
```

Each `.txt` label file follows the YOLO bounding box format:

```
class_id  x_center  y_center  width  height
```

All coordinates are normalized to `[0,1]`.

---

## Use Cases
These annotations enable research on:

- Omni-directional object detection  
- Spherical and equirectangular deep learning  
- Small object detection in 4K panoramic footage  
- Real-time 360° surveillance and robotics  
- Depth-aware detection when combined with the original CVIP360 depth maps

---

## Citation
If you use this annotation set in your research, please cite both this repository and the original CVIP360 dataset.

### **BibTeX (for this annotation project)**

```bibtex
@dataset{Hafeez2025BBoxCVIP360,
  author       = {Huma Hafeez},
  title        = {CVIP360-Based Bounding Box Annotations for Omni-Directional Object Detection},
  year         = {2025},
  publisher    = {GitHub},
  journal      = {GitHub Repository},
  howpublished = {\url{https://github.com/<your-repo-link>}},
  note         = {Custom YOLO-format annotations built on top of the CVIP360 dataset},
}
```

### **BibTeX (CVIP360 Dataset – include this in papers)**  
*(Replace with the official citation if you prefer)*

```bibtex
@article{cvip360,
  title     = {CVIP360: A Panoramic Vision Dataset for Depth Estimation and Scene Understanding},
  author    = {Original CVIP360 Authors},
  journal   = {arXiv preprint},
  year      = {2020}
}
```

---

## License
These annotations are released for **research and academic use**.  
Please ensure compliance with the **original CVIP360 dataset license** before redistribution.

---

## Acknowledgements
- **CVIP360 dataset authors** for providing high-quality 360° panoramic images and depth maps.
- The research community developing spherical CNNs and equirectangular detection models.

---

## Contact
For questions or collaborations, feel free to open an issue or contact:

**Huma Hafeez**  
Real-time 360° Object Tracking & Detection Researcher  
```
<huma.asad918@yahoo.com>
```



