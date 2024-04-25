# Seagrass-Detection
Marine Science project <br />
Dataset: Drone footage of various Auckland North-shore beaches (SnellsBeach, Sandspit, Brickbay) <br />
Training and evaluating Machine Learning models (SVD, Decision Trees, Naive Bayes, Random Forest, and XGBoost) and Deep Learning models (MLP and U-Net) for Seagrass Detection<br />

The below shows two samples of the dataset and their annotated seagrass regions. <br />
![dataset-sample](https://github.com/shahrokh1106/Seagrass-Detection/assets/44213732/13ba6c2d-90c0-4383-886e-8ea47fea5d4e) <br />

The main goal was to train a model to detect seagrass regions, resulting in the number of seagrass pixels in each frame. The number of seagrass pixels in the computed orthophotos is converted to the meter unit based on the camera calibration parameters to estimate the area of the detected regions in each beach in the dataset. This repository only provides the trained models, with some sample codes for training. We obtained the best result from a U-net CNN based on a patch-based approach. The following shows a bit more details for the U-Net setup and some prediction results.<br />

•	Total number of total images in the dataset: 308 (each with size 3456 × 4068)<br />
•	Cropping each image to (3328 × 4068) to have (256 × 256) patches<br />
•	Dividing each image to 13×18 = 234 patches<br />
•	The number of images in the new dataset: 308 × 234 = 72,072<br />
•	Splitting the new dataset into the training set (0.8), validation set (0.1), and test set (0.1)<br />
  o	training set = 57,657 patches<br />
  o	validation set = 7,201 patches<br />
  o	test set = 7,201 patches<br />

![U-Net-Preds](https://github.com/shahrokh1106/Seagrass-Detection/assets/44213732/dd57f84c-ac88-4907-9061-594ea61a3724)




