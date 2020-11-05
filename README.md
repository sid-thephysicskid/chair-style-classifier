# Chair_Style_classifier

As a hobbyist woodworker, I can't help but drool everytime I come across a handcut dovetail joint of a keepsake box, or delectable tenons of a handcrafted chair. What's not trivially obvious sometimes, is the style of a piece of furniture or the period whence its inspired from. 
Sure its easier to tell a victorian chair from a contemporary chair, but is the contemporary chair 'mid century modern' or 'art deco'? Or does it draw some inspirations from a shaker period? Thought it'd be a fun project to explore if a machine can learn to classify such subtle features that go beyond mere geometrical features of two chairs.

This project is the first of possibly many attempts to see if a CNNs can accomplish the task. Intuitively, I expect this project to go into the realms of Fine-Grain Image classification, using Bilinear CNNs (BCNNs) but I'll start with something simpler first.

The Train-chair-style.ipynb notebook features a smaller problem of training a CNN to distinguish and classify 5 different styles of chairs, namely 'Farmhouse', 'Industrial', 'MidCentury', 'Tropical', and 'Victorian'. 

The input is a fairly small data set of about ~2200 net pictures of chairs that belong to 5 categories. Source: https://cvml.comp.nus.edu.sg/furniture/index.html

I will use transfer learning on MobilenetV2 trained on Imagenet data, and fine tune it.

Since mere validation accuracy would be a poor predictor for a multi-class image classification such as this, the performance metric will be multi-class logarithmic loss. A confusion matrix should help in visualizing the performance. 

