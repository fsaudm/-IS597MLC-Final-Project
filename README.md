# IS597MLC-Final-Project


The dataset in this repo is a fraction of the original (much bigger) dataset: *SODA: A large-scale open site object detection dataset for deep learning in construction*, from Rui Duan, Hui Deng, Mao Tian, Yichuan Deng, Jiarui Lin. (https://www.sciencedirect.com/science/article/abs/pii/S0926580522003727)

This curated, "bite-sized" dataset for this project contains:
- 1000 images with labels for training
- 100 images with labels for testing

The images are in .jpg format, and the labels have been transformed to .txt, but these were originally in .xml files (the corresponding files are included as well). It is important to understand that the format of the labels expected by these models is of the form:


| label | x-coord | y-coord | width | height |
|-------|---------|---------|-------|--------|
|   1   |   0.5   |   0.5   |  0.25 |  0.25  |


- **label**: The class label of the object (numbers)
- **x-coord**: Normalized x-coordinate of the bounding box
- **y-coord**: Normalized y-coordinate of the bounding box
- **width**: Normalized width of the bounding box
- **height**: Normalized height of the bounding box


<br>

## **YOLOv10**
The best results for this model were achieved with the pretrained version `yolov10n.pt`:
![Results](IS597MLC-Final-Project/runs/detect/results_yolo10_pretrained/results.png)

<br>

For this model, the **normalized confusion matrix**:
![Confusion Matrix](IS597MLC-Final-Project/runs/detect/results_yolo10_pretrained/confusion_matrix_normalized.png)


<br>

## **DeTr**
The best results for the DeTr were achieved with the pretrained version `rtdetr-l.pt`:
![Results](IS597MLC-Final-Project/runs/detect/results_detr_pretrained/results.png)


<br>

, and this is the **normalized confusion matrix**:
![Confusion Matrix](IS597MLC-Final-Project/runs/detect/results_detr_pretrained/confusion_matrix_normalized.png)
