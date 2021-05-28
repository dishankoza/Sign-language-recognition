# Sign-language-recognition

This project is a sign language gesture recognizer using Python, openCV and tensorflow for training InceptionV3 model, a convolutional neural network model for classification.

The framework used for the CNN implementation can be found here:

[Simple transfer learning with an Inception V3 architecture model](https://github.com/xuetsing/image-classification-tensorflow) by xuetsing

If you are only interested in code, you better copy/paste the few files than cloning the entire project.

You can [find the demo here](https://drive.google.com/file/d/1I_q5PdrdlQyiN-sj0xM9HUim-l-OF6D8/view?usp=sharing)

## Requirements

This project uses python 3.5 and the PIP following packages:
* opencv
* tensorflow
* matplotlib
* numpy

## Training

To train the model, use the following command (see framework github link for more command options):
```
python3 train.py \
  --bottleneck_dir=logs/bottlenecks \
  --how_many_training_steps=2000 \
  --model_dir=inception \
  --summaries_dir=logs/training_summaries/basic \
  --output_graph=logs/trained_graph.pb \
  --output_labels=logs/trained_labels.txt \
  --image_dir=./dataset
  
To test classification, use the following command:
```
python3 classify.py path/to/image.jpg
```
## Using webcam (demo)
```
To use webcam, use the following command:
```
python3 classify_webcam.py
```
