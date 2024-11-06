# Classifying Lions and Tigers


The project was to use CNNs to classify between a lion and a tiger using the Keras API as part of my Deep Learning (DLE305) course.

## Process
1. Instead of training a model on lion and tiger (let's call it model-1) images from the ground up, I trained an initial model on cat and dog images (let's call this model-2) on the presumption that both sets of animals have similar features (whiskers, nose, face structure). The conv layers in model-2 should learn features that help predict lions and tigers.
2. The conv layers from model-2 are frozen and used as the initial layers for model-1 followed by Dense MLP layers.
3. Another variant of model-1 is trained using image augmentation that helps the model generalise better with different orientations, brightness, zoom, etc.

## Findings
1. Writing util functions in notebooks is something I wouldn't wish upon anyone.
2. Model-1 has an average F1 score of ~68%, which is quite well considering we used model-2 as a feature extractor trained on a completely different dataset.
3. Model-1 with augmentation shows an even higher score of ~71%, meaning, it works!

## Future Work
I want to try visualising the convolutional layers and see what features are learned. It seems interesting.
