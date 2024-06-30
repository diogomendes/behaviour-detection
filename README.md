# Project Compatibility and Requirements

## Operating Systems:

Compatible with Windows and Linux

## Dependencies:

Python 3.11.9
pandas 2.2.1
torch 2.2.1+cu121
torchvision 0.17.1
matplotlib 3.8.3
numpy 1.24.4
imageio 2.34.0
tqdm 4.66.2
torchmetrics 1.3.2

## Instructions to Run the Code:

### Installation of Dependencies

### Structure of the Project:
The programs are located in the pig_tracking folder:

extract_frames.py: Extracts frames from a video at specified intervals (e.g., 30 seconds, 1 minute, etc.).

data_act.py: Prepares the data by analyzing the frames and assigning actions to each bounding box.

train_act.py: Main program for training the model with a specified number of epochs and pigs. This script also handles testing and saves training images as a GIF to visualize the results.

model_act.py: Contains the implementation of the model used.

### Execution of the Code:

#### Extract Frames from Video:
To extract frames from a video, use:

python extract_frames.py or python3 extract_frames.py

#### Prepare Data:
Use LabelMe to detect pig positions by drawing bounding boxes around them. Save the annotations in the appropriate format.

#### Train the Model:
To train the model, run:

python train_act.py or python3 train_act.py

You can specify the number of epochs and the number of pigs within this script.

#### Model Implementation:
The model's architecture and logic are contained in model_act.py. This script is imported and used by train_act.py.

## Notes:
extract_frames.py and train_act.py are the primary scripts to be executed.

Ensure all required libraries are installed and properly configured.

Customize parameters such as the number of epochs and pigs directly within the respective scripts.


## Results
After training the model, we conducted several tests to evaluate its performance. Below, we showcase some examples of the model's predictions, highlighting both its best and worst cases. These examples help illustrate the model's strengths and areas for improvement.

### Best Predictions
Here are some instances where the model performed exceptionally well. The predictions closely match the actual labels, demonstrating the model's capability in accurate detection and classification:

![best_frame](https://github.com/diogomendes/Behaviour-recognition/assets/164574855/ba93595a-21ae-4073-873b-7c840b3b3c09)


### Worst Predictions
In contrast, the following examples highlight some of the challenges the model faced. These predictions were not as accurate, indicating potential areas for further refinement and training:

![Worst_frame](https://github.com/diogomendes/Behaviour-recognition/assets/164574855/c7f51a80-10c5-486f-85a1-483a1b823216)


### Cross-Environment Performance
To assess the model's adaptability, we tested it on images from environments different from those used in training. The following examples illustrate the model's performance in these new settings. The results indicate that the model struggles to maintain accuracy when faced with unfamiliar environments, suggesting that it is not well-adapted for generalization beyond its training data:

![new_env](https://github.com/diogomendes/Behaviour-recognition/assets/164574855/45b0d402-f224-4893-9a3c-81896a00232d)


## Conclusion
The visualizations above provide insight into the model's performance. While it demonstrates strong predictive capability in many cases, there are still scenarios that require improvement. Ongoing adjustments and additional training data may help enhance accuracy and robustness.

Feel free to explore the code and experiment with the model to achieve even better results!
