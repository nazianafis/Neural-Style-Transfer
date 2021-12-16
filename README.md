# Neural-Style-Transfer (NST)

This repo contains a lightweight PyTorch implementation of the paper :link: [Gatys et al.](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf).

![](https://github.com/nazianafis/NST/blob/main/misc/NST.gif)

## Table of Contents

1. [Overview](#overview)
2. [File Description](#description)
3. [Getting Started](#getting-started)
    1. [Dependencies](#dependencies)
    2. [Installation](#installation)
4. [Output](#output)
5. [Acknowledgements](#ack)

## Overview <a name="overview"></a>

Neural style transfer is an optimization technique used to take two images—a content image and a style reference image (such as an artwork by a famous painter)—and blend them together so the output image looks like the content image, but “painted” in the style of the style reference image.

## Getting Started <a name="getting-started"></a>

### File Description <a name="description"></a>
    Neural-Style-Transfer
        ├── NST.py
        ├── data
        |   ├── content-images
        |   ├── style-images
        |   ├── output-images
        ├── models/definitions     
        │   ├── __pycache__
        │   ├── vgg_nets.py
        ├── misc
        ├── LICENSE
        └── README.md

### Dependencies <a name="dependencies"></a>
*    Python 3.9+
*    Framework: PyTorch
*    Libraries: os, numpy, cv2, matplotlib

### Installation <a name="installation"></a>

#### To run the project:

1. Clone the repository and move to the downloaded folder:
```
    $  git clone https://github.com/nazianafis/Neural-Style-Transfer
    $  cd Neural-Style-Transfer
```
2. Go to `NST.py`, and in it, set the `PATH` variable to your downloaded folder:
```
    $ PATH = <your_path>
```
3. Run `NST.py`:
```
    $ python NST.py
```
#### To try Neural Style Transfer on images of your own:

1. Clone the repository and move to the downloaded folder:
```
    $  git clone https://github.com/nazianafis/Neural-Style-Transfer
    $  cd Neural-Style-Transfer
```
2. Move your content/style image(s) to their respective folders inside the `data` folder.

3. Go to `NST.py`, and in it, set the `PATH` variable to your downloaded folder. Also set `CONTENT_IMAGE`, `STYLE_IMAGE` variables:
```
    $ PATH = <your_path>
    
    $ CONTENT_IMAGE = <your_content_image_name>
    $ STYLE_IMAGE = <you_style_image_name>
```
4. Run `NST.py`:
```
    $ python NST.py
```

## Output <a name="output"></a>


<img src="https://github.com/nazianafis/Neural-Style-Transfer/blob/main/data/content-images/c1.jpg" alt="content" width="222"/> <img src="https://github.com/nazianafis/Neural-Style-Transfer/blob/main/data/style-images/s1.jpg" alt="style" width="273"/> <img src="https://github.com/nazianafis/NST.github.io/blob/main/data/output-images/c1/c1_s1.jpg" alt="output" width="222"/>

<br>

<img src="https://github.com/nazianafis/Neural-Style-Transfer/blob/main/data/content-images/c1.jpg" alt="content" width="222"/> <img src="https://github.com/nazianafis/Neural-Style-Transfer/blob/main/data/style-images/s2.jpg" alt="style" width="356"/> <img src="https://github.com/nazianafis/NST.github.io/blob/main/data/output-images/c1/c1_s2.jpg" alt="output" width="222"/>

<br>

<img src="https://github.com/nazianafis/Neural-Style-Transfer/blob/main/data/content-images/c1.jpg" alt="content" width="222"/> <img src="https://github.com/nazianafis/Neural-Style-Transfer/blob/main/data/style-images/s5.jpg" alt="style" width="333"/> <img src="https://github.com/nazianafis/NST.github.io/blob/main/data/output-images/c1/c1_s5.jpg" alt="output" width="222"/>

<br>

<img src="https://github.com/nazianafis/Neural-Style-Transfer/blob/main/data/content-images/c1.jpg" alt="content" width="222"/> <img src="https://github.com/nazianafis/Neural-Style-Transfer/blob/main/data/style-images/s6.jpg" alt="style" width="282"/> <img src="https://github.com/nazianafis/NST.github.io/blob/main/data/output-images/c1/c1_s6.jpg" alt="output" width="222"/>

All of the following outputs were generated using the code in this repository, with no other image manipulation. 
<br><br>


## Acknowledgements <a name="ack"></a>

I found these sources of great help during the making of this project:
* The original paper on neural style transfer by [Gatys et al](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf) 
* Aleksa Gordic's [implementation](https://github.com/gordicaleksa/pytorch-neural-style-transfer)
* PyTorch's [Tutorial on NST](https://pytorch.org/tutorials/advanced/neural_style_tutorial.html)
* The original paper on [VGG19](https://arxiv.org/abs/1409.1556)

All of the content/style images have been taken from here:
* [Unsplash](https://unsplash.com/)
* [Wikimedia](https://commons.wikimedia.org/wiki/Category:Images)

