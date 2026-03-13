# Comparative Study of Image Segmentation Algorithms

This project implements and evaluates several **image segmentation algorithms** for multi-class segmentation of MRI images. The goal is to compare performance and identify the most effective method using appropriate evaluation metrics.

---

## Aims

Image segmentation is the process of partitioning an image into multiple coherent regions based on pixel- or object-level characteristics. Segmentation algorithms typically work by:

- Detecting boundaries between regions (e.g., edge-based, thresholding)  
- Grouping features with similar properties (e.g., clustering, region growing)  
- A combination of both  

This study focuses on **multi-class segmentation** rather than binary segmentation. The project aims to:

1. Implement, investigate, and analyze various 2D segmentation algorithms for MRI images:  
   - Thresholding  
   - Multi-Otsu Thresholding  
   - K-Means Clustering  
   - Mean-Shift Clustering  

2. Evaluate the performance of the segmentation algorithms using a suitable metric to identify the most effective method relative to ground truth images.  

3. Explore the differences in segmentation performance between **iterative 2D segmentation** and **simultaneous 3D segmentation**.

---

## Methodology

- **Preprocessing**: Applied techniques such as active contours to detect boundaries and improve mask quality.  
- **Segmentation**: Implemented thresholding, Multi-Otsu Thresholding, K-Means, and Mean-Shift Clustering.  
- **Evaluation Metric**: Used **F1-score** instead of standard pixel accuracy to handle imbalanced regions in MRI images.  
- **Comparative Analysis**: Tested segmentation on individual 2D slices iteratively and compared with simultaneous 3D segmentation approaches.

---

## Results & Conclusions

- **Most Effective Algorithm**: Multi-Otsu Thresholding consistently provided the best segmentation results.  
- **Clustering Performance**: Mean-Shift Clustering performed better than K-Means, but slightly worse than Multi-Otsu.  
- **Preprocessing Impact**: Active contour-based mask refinement significantly enhanced segmentation accuracy.  
- **2D vs 3D Segmentation**: 3D segmentation reduced computational cost but slightly compromised accuracy compared to iterative 2D segmentation.  

---

## Tools & Libraries

- Python 3.x  
- OpenCV  
- scikit-image  
- NumPy, pandas, Matplotlib / Seaborn for visualization  

---

## Notes

- This project focuses on **research and educational purposes** rather than clinical deployment.  
- The comparative framework can be extended to other types of medical imaging or multi-class segmentation tasks.
