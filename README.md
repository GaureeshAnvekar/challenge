
# CHALLENGE EXERCISE


### Problem

Objective  is to apply the style of an image, which we will term as
"style image" to a target image while preserving the content of the
target image.


 - **Style** is textures and visual patterns in an image. Example is
   brush strokes of an artist
 - **Content** is the macro structure of an image, like buildings,
   people, objects in the content of the image.

### High Level Steps
 - choose the image to style
 - choose the style reference image (here we have provided a Picasso style image)
 - choose a pre-trained deep neural network (CNN type) and obtain
   feature representations of intermediate layers. This step is done
   to achieve the representations of both the content image and style
   image. For the content image, best option is to obtain the feature
   representations of highest layers as they would contain information
   on the image macro-structure. For the style reference image, feature
   representations are obtained from multiple layers at different
   scales.
 - define loss function
 -  **Loss** function should be taking into account the Content-loss, Style-loss, Variation-loss.
 - /Optimize on each iteration to minimize the loss/


#### Recommended Overview  of the steps generally followed
  - Create a random input image
  - Pass the input through a pre-trained backbone architecture
  - Calculate loss and compute the gradients w.r.t input image
    pixels. Hence only the input pixels are adjusted whereas the
    weights remain constant.

#####  *This problem consists of two sub problems:*
  1. to generate the content and 
   
  2. to generate the style    

###### SubProblem — 1. Generate Content
The problem is to produce an image that contains a content as in the
content image.

*General Guideline* 

One point to note here is that the image should only contain the
content(as in a rough sketch of the content image and not the texture
from the content image, since the output should contain a style
different from the style image)


######  SubProblem — 2. Generate Style
The problem is to produce an image which contains the style as in the
style image.  

*General Guideline*

Compute **MSE loss between gram matrix of input and the style image** and
you should be good to generate an input image with the required style.
Publish the model details, output results and model metrics.

###  Scoring 

Each participating team will be scored on the implementation of the
machine learning model. The short listed teams will undergo tcon to
guage their understanding of the nuances of the model and its
architecture, understanding of library calls invoked, and expertise of
language constructs.

### Content Image : japanese_garden.jpg (in this repo)
### Style image   : picasso_selfportrait.jpg (in this repo)




