# Cycle_GAN_tutorial_practice
Application of CycleGAN Tutorial

This notebook is a customized practice application on CycleGAN. 
It follows the training instruction from official CycleGAN tutorial from Google Research:
https://colab.research.google.com/github/tensorflow/docs/blob/master/site/en/tutorials/generative/cyclegan.ipynb#scrollTo=_xnMOsbqHz61

## Image Transformation

This project refers to the original CycleGAN repo: https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix.

Cycle GAN transforms image from one domain, to another domain. Unlike traditional GAN, it forces reconstruction of image to original domain to be similar to the input, by adding Cycle-Loss

![image](https://user-images.githubusercontent.com/43837843/122640665-b8e19800-d13b-11eb-930e-7751ea2ac402.png)

## Project Description

Using google-tutorial notebook of Cycle-GAN, this project train a model to transform scenary style to japanese-animated scenary styled
Input domain data (real scenary) are random 300 selection of Cycle-GAN official repo training dataset.
Transformation domain data (animated) are scraped from google image.

![image2](https://user-images.githubusercontent.com/43837843/122640726-0bbb4f80-d13c-11eb-802d-1675f780f1c6.png)

## Some Lessons & Improvements

* Since 1) dataset in general was low-quality,  2) variance (variety) of each image was not large, and 3) entire dataset size was small, extreme small-batch of size 1 worked well for the case. 
* Since generator generate image from the random noise, it works better when giving comparatively higher learning rate for generator, compared to discriminator
* For improvement, I would like to augment the dataset in the future project

![image3](https://user-images.githubusercontent.com/43837843/122640741-1b3a9880-d13c-11eb-836e-39427994d11c.png)

## Example outcome

![image4](https://user-images.githubusercontent.com/43837843/122640878-b7fd3600-d13c-11eb-8822-daabd6b7f857.png)

