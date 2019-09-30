# KAIST Multispectral Depth Estimation:

This Repository contains code for Depth Estimation using IR images </br>
It has been tested on GTX 1080ti and tensorflow 1.13 and contains scripts for both inference and training .</br>

## RGB-IR Encoder Decoder Network

![](RGBIR_ENCDEC.png)

The project was built on Python-3.6.7 and requires following packages

* ```matplotlib==3.0.2```
* ```numpy==1.16.2```
* ```opencv-python==4.0.0.21```
* ```tensorboard==1.13.1```
* ```tensorflow-gpu==1.13.1```
* ```tqdm==4.31.1```

## Results Day

![](gifs/day_depth.gif)


## Results Night

![](gifs/night_depth.gif)

## Test on Single Image:

Use script test_single.py to perform inference. The script expects : </br>
1. Please copy test images to the RGB-IR EncDec/demos directory, the resulting output is stored in demos/predictions </br>
2. Run the below script from tools directory </br>
3. Download pretrained model [here](https://drive.google.com/open?id=1hYcr-SoBeUQn55Lwh_vY3a3FiBsdWTIu) and place it in model/enc-dec  </br>
4. If save is changed to 0, then images will be displayed not saved.  </br>

### Sample Command:
```
python test_image.py --img_name set09_V000_I03399.jpg --save 1
```

## Training Instructions:

### Script tools\train_model.py trains RGB-IR EncDec model. </br>

#### Description of inputs to the script: 

1. If existing checkpoint is found, training resumes from there. Else training starts from scratch. Directory names for logs and saved checkpoints can be changed in the script. </br>

## Testing Instructions:

### Script tools\test_model tests model. </br>

#### Description of inputs to the script: 

1. Model is loaded from existing checkpoint. Directory names for saved checkpoints can be changed in the script. </br>
2. Download pretrained model [here](https://drive.google.com/open?id=1hYcr-SoBeUQn55Lwh_vY3a3FiBsdWTIu) and place it in model/enc-dec  </br>

### Sample Command:
```
python test_model.py
```



