<br>
<img src="https://github.com/nazianafis/Neural-Style-Transfer/blob/main/misc/NST-gif.gif" alt="header" align="right" width="270"/>

# Neural-Style-Transfer (NST)

Neural Style Transfer is the ability to create a new image (known as a pastiche) based on two input images: one representing the content and the other representing the artistic style.

This repository contains a lightweight PyTorch implementation of the seminal paper on neural style transfer by [Gatys et al.](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf) To make the model faster and more accurate, a pre-trained VGG19 model is used.

## Table of Contents

1. [Overview](#overview)
2. [How does it work?](#working)
3. [File Description](#description)
4. [Getting Started](#getting-started)
    1. [Dependencies](#dependencies)
    2. [Installation](#installation)
5. [Output](#output)
6. [Acknowledgements](#ack)

## Overview <a name="overview"></a>

Neural style transfer is a technique that is used to take two images—a content image and a style reference image—and blend them together so that output image looks like the content image, but “painted” in the style of the style reference image.

## How does it work?<a name="working"></a>

1. We take content and style images as input and pre-process them.
2. Next, we load VGG19 which is a pre-trained CNN (convolutional neural network).
    1. Starting from the network's input layer, the first few layer activations represent low-level features like colors, and textures. As we step through the network, the final few layers represent higher-level features—like eyes.
    2. In this case, we use `conv1_1`, `conv2_1`, `conv3_1`, `conv4_1`, `conv5_1` for style representation, and `conv4_2` for content representation.    
![](https://github.com/nazianafis/Neural-Style-Transfer/blob/main/misc/NST-architecture.png)

3. We begin by cloning the content image and then iteratively changing its style. Then, we set our task as an optimization problem where we try to minimize:
    1. **content loss**, which is the L2 distance between the content and the generated image,
    2. **style loss**, which is the sum of L2 distances between the Gram matrices of the representations of the content image and the style image, extracted from different layers of VGG19.
    3. **total variation**, which is used for spatial continuity between the pixels of the generated image, thereby denoising it and giving it visual coherence.
4. Finally, we set our gradients and optimize using the L-BFGS algorithm to get the desired output.

## Getting Started <a name="getting-started"></a>

### File Description <a name="description"></a>

    Neural-Style-Transfer
        |
        ├── data
        |   ├── content-images
        |   ├── style-images
        ├── NST.py  <-- the main python file
        ├── models/definitions     
        │   ├── vgg19.py   <-- VGG19 model definition
        ├── misc
        ├── LICENSE
        └── README.md

### Dependencies <a name="dependencies"></a>
*    Python 3.9+
*    Framework: PyTorch
*    Libraries: os, numpy, cv2, matplotlib

### Installation <a name="installation"></a>

#### To try Neural Style Transfer on images of your own:

1. Clone the repository and move to the downloaded folder:
```
    $  git clone https://github.com/nazianafis/Neural-Style-Transfer
```
```
    $  cd Neural-Style-Transfer
```
2. Move your content/style image(s) to their respective folders inside the `data` folder.

3. Go to `NST.py`, and in it, set the `PATH` variable to your downloaded folder. Also set `CONTENT_IMAGE`, `STYLE_IMAGE` variables as your desired images:
```
    $ PATH = <your_path>
   
    $ CONTENT_IMAGE = <your_content_image_name>
    $ STYLE_IMAGE = <you_style_image_name>
```
4. Run `NST.py`:
```
    $ python NST.py
```
5. Find your generated image in the `output-images` folder inside `data`.

## Output <a name="output"></a>

<img src="https://github.com/nazianafis/Neural-Style-Transfer/blob/main/misc/NST-outputs.png" alt="content" width="700"/>
(All outputs were generated using the code in this repository.)
<br><br>


## Acknowledgements <a name="ack"></a>

* PyTorch's [tutorial on NST](https://pytorch.org/tutorials/advanced/neural_style_tutorial.html)
* Aleksa Gordic's [implementation](https://github.com/gordicaleksa/pytorch-neural-style-transfer)
* The original paper on neural style transfer by [Gatys et al](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf) 
* The original paper on [VGG19](https://arxiv.org/abs/1409.1556)
* Cat against the blue background photo by <a href="https://unsplash.com/@cedric_photography?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Cédric VT</a> on <a href="https://unsplash.com/s/photos/cat?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
* All other content/style images from [Wikimedia](https://commons.wikimedia.org/wiki/Category:Images), [Unsplash](https://unsplash.com/).

