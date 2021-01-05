# HW4_Image-Super-Resolution

### **Introduce —**
Super-Resolution: 
* Implementation of Enhanced Deep Residual Networks for Single Image Super-Resolution
* Training set: 291 high-resolution images
* Testing set: 14 low-resolution images

### **Hardware —**
* Tensorflow 1.15.2

### **Reproducing Submission —**
> 1. Dataset Preparation
> 2. Training
> 3. Inference

#### 1. Dataset Preparation
> Use ```augmentation.py``` to do data augmetation on training dataset.
>> change the value of ```augment_level``` in  augmentation.py
>>
>> In this project, I set ```augment_level = 8``` to generate eight times the training images

#### 2. Training
> 1.) First, you need to  ```cd EDSR_Tensorflow/```.
>
> 2.) Then, you need to compute the RGB mean. Using the ```calcmean``` in ```data_utils.py``` and change the ```meanbgr``` value in ```main.py```.
>
> 3.) If you want to start training from scratch, you can use
>
>     python main.py --train --fromscratch --scale <scale> --epochs <epochs> --traindir <path to training dataset> --validdir <path to testing dataset>
>
> 4.) If you want to resume training, you can use
>
>     python main.py --train --scale <scale> --epochs <epochs> --traindir <path to training dataset> --validdir <path to testing dataset>
>
> 5.) In this project, I train the EDSR with 30 epochs.
  
#### 3. Inference
> 1.) Change the ```folder``` and ```the number of testing images``` in the **test** function of  ```run.py```
>
> 2.) Start inference: ```python main.py --test --scale <scale>```
  
### **Results —**
left: bicubic / Right: EDSR

<img src="https://github.com/ChihChia-Li/HW4_Image-Super-Resolution/blob/main/EDSR_Tensorflow/Results_example/02_bicubic.png" width="20%" height="20%" />   <img src="https://github.com/ChihChia-Li/HW4_Image-Super-Resolution/blob/main/EDSR_Tensorflow/Results_example/02_edsr.png" width="20%" height="20%" />


### **Reference —**
https://github.com/Saafke/EDSR_Tensorflow



 
