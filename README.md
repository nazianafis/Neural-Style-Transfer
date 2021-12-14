# Neural-Style-Transfer (NST)

This repo contains a lightweight PyTorch implementation of the paper :link: [Gatys et al.](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf).

![](https://github.com/nazianafis/NST/blob/main/misc/NST.gif)

## Table of Contents

1. [Overview](#overview)
2. [File Description](description)
3. [Getting Started](#getting-started)
    1. [Dependencies](#dependencies)
    2. [Installation](#installation)
4. [Acknowledgements](#ack)

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
*    Libraries: Numpy, cv2, PyTorch
*    Data Visualization: Matplotlib

### Installation <a name="installation"></a>

#### To run the project:

Clone the repository:
```
  $  git clone https://github.com/nazianafis/Neural-Style-Transfer
```
Run the 'NST.py':
```
  $ python NST.py
```

## Acknowledgements <a name="ack"></a>

I found these sources of great help during the making of this project:
* [Aleksa Gordic](https://github.com/gordicaleksa/pytorch-neural-style-transfer)
* [PyTorch](https://pytorch.org/tutorials/advanced/neural_style_tutorial.html)
* [Tensorflow](https://www.tensorflow.org/tutorials/generative/style_transfer)

I found all of the content/style images from here:
* [Unsplash](https://unsplash.com/)
* [Wikimedia](https://commons.wikimedia.org/wiki/Category:Images)

