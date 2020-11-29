##--Work in progress
# Inspiration
As a hobbyist woodworker, I can't help but drool everytime I come across dovetail joints of a keepsake box, or delectable tenons of a handcrafted chair. What's not trivially obvious sometimes, is the style of a piece of furniture or the period whence its inspired from. 

Figured it'd be a fun project to explore if a machine can learn to classify furniture styles, for example distinguish a 'midcentury desk' from a 'farmhouse desk'. This would be more involved than standard cat vs dog classifiers because the distinctions between furniture styles relies on more subtle features that go beyond mere geometry and shape.

This project is the first attempt to see if a CNN can accomplish the task. Intuitively, I expect this project to go into the realms of Fine-Grain Image classification, using Bilinear CNNs (BCNNs) but I'll start with something simpler first.

# Project
The Train-chair-style.ipynb notebook features a smaller problem of training a CNN to distinguish and classify 4 different styles of chairs, namely 'Farmhouse', 'Industrial', 'MidCentury', and 'Tropical'.

The input is a fairly small data set of about 1900 pictures of chairs that belong to those 4 categories, more or less equally distributed amongst the 4 classes. Source: https://cvml.comp.nus.edu.sg/furniture/index.html

I will use transfer learning on MobilenetV2 trained on Imagenet data, and fine tune it.

Since mere validation accuracy would be a poor predictor for a multi-class image classification such as this, a confusion matrix should help in visualizing the performance. 

(Perhaps include the multi-class logarithmic loss?)

# Deployment 
Flask + AWS? 
