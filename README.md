## Reimplementation of Gatys et Al
In this notebook, we’ll recreate a style transfer method that is outlined in the paper, Image Style Transfer Using Convolutional Neural Networks, by Gatys in PyTorch.
In this paper, style transfer uses the features found in the 19-layer VGG Network, which is comprised of a series of convolutional and pooling layers, and a few fully-connected layers. In the image below, the convolutional layers are named by stack and their order in the stack.

Link for the paper https://arxiv.org/abs/1508.06576

## Separating Style and Content

Style transfer relies on separating the content and style of an image. Given one content image and one style image, we aim to create a new, target image which should contain our desired content and style components:
-  objects and their arrangement are similar to that of the content image
- style, colors, and textures are similar to that of the style image

## Input Files
As input we'll take the style of _Starry Night by Van Gogh_, and use the content of a group image with my best friends.
<img src="https://github.com/youssefokeil/Gatys-et-Al-reimplementation/blob/main/input_images/starry_night.jpg" alt="starry_image" width="600"/>
<img src="https://github.com/youssefokeil/Gatys-et-Al-reimplementation/blob/main/input_images/pre_germany.JPG" alt="boys_image" width="600"/>

## Output Files
The output of blending the style of Van Gogh with the group photo is:

![starry_men](https://github.com/youssefokeil/Gatys-et-Al-reimplementation/blob/main/output/starry_men.jpg)
