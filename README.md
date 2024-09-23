Kaggle dataset: https://www.kaggle.com/datasets/deathtrooper/glaucoma-dataset-eyepacs-airogs-light-v2


Experiments and Result

We use the Rotterdam EyePACS AIROGS dataset (in full, including train and test) contains 113,893 color fundus images from 60,357 subjects and approximately 500 different sites with a heterogeneous ethnicity. All images were assigned by human experts with the labels referable glaucoma, no referable glaucoma, or ungradable. The training set can be downloaded at kaggle dataset: Glaucoma Dataset: EyePACS-AIROGS-light-V2.

This is an improved machine-learning-ready glaucoma dataset using a balanced subset of standardized fundus images from the Rotterdam EyePACS AIROGS set. This dataset is split into training, validation, and test folders which contain 4000 (~84%), 385 (~8%), and 385 (~8%) fundus images in each class respectively. Each training set has a folder for each class: referable glaucoma (RG) and non-referable glaucoma (NRG)

The dataset has 3 folders which are: test, train, validation. Each folder has an NRG, NG subfolder which stand for referable glaucoma (RG) and non-referable glaucoma (NRG). 
We collect all those image paths together and then encode RG as 1 and NRG as 0.

We have benchmarks with 4 models which are: Vision Transformer, Resnet50, Swin Transformer, Resnet50 and EfficientNetB5.

Table 1: Benchmark models with other models

||1st|2nd|3rd|4th|5th|
|---|---|---|---|---|---|
|Swin Transformer|0.926250|0.920625|0.925625|0.922500|0.929400|
|Resnet50|0.917500|0.913750|0.919375|0.916250|0.906250|
|Vision Transformer|0.858125|0.858125|0.84875|0.83500|0.848800|
|EfficientNetB5|0.916875|0.916250|0.918750|0.908125|0.917500|

\
![alt text](<imgs/W&B Chart 9_23_2024, 2_36_03 PM.png>)
![alt text](<imgs/W&B Chart 9_23_2024, 2_36_17 PM.png>)
![alt text](<imgs/W&B Chart 9_23_2024, 2_36_27 PM.png>)

Through the experiment, Swin Transformer is the fastest and has the most accuracy 