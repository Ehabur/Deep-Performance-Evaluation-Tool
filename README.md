## Instructions to use the evaluation routine on other object detection models:

This project aims to provide the results in COCO dataset for different object detection models styles like Masked R-CNN, YOLO  & SSD.

There will be the explanation and the abstract for the project here.



You can easily evaluate your different object detection models on any dataset with Evaluate_Models notebook. To do this, predictions of your model and groundtruth information must be saved separately in .txt files and match the below format:



**image_id,class_id,[y1 x1 y2 x2]* **

*: bounding box coordinates are not in a python list but numpy array. If you have a list, simply convert it to numpy array for convenience.


Each line which stores a single bounding box information, must be ordered by the image_id. Examples of the expected input files are provided under the *demo/vallogs* directory with the names of **"gt.txt"** and **"preds.txt"**. Since it takes some time to obtain the output of the model for every single image in big datasets like COCO, it is crucial to save the results and  is the reason why this routine needs them as input files.

After generating the input files, simply open *Evaluate_Models.ipynb* and follow the instructions in the notebook to evaluate your own models. You may change the parameters such as IoU_threshold according to your needs as explained in the notebook. Plottings and figures will be created and saved under this directory.
