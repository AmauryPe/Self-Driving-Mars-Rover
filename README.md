# Self-Driving-Mars-Rover

**Introduction:**

This repository contains a neural network to classify pixels of images taken on the surface of Mars by rovers. It uses the AI4Mars dataset, a comprehensive collection designed for training and validating terrain classification models tailored for Mars rovers. The motivation behind this project stems from the observation that, while classical machine vision systems have been pivotal for Mars rovers, the integration of deep learning capabilities, such as semantic segmentation and object recognition, could significantly enhance safety and productivity during Mars missions.

The AI4Mars dataset comprises approximately 326,000 labeled semantic segmentation full image labels across 35,000 images captured by the Curiosity, Opportunity, and Spirit rovers. These images were meticulously labeled through crowdsourcing, involving around 10 contributors per image to ensure label quality and consensus. Additionally, the dataset includes 1,500 validation labels annotated by experts from NASA’s Mars Science Laboratory (MSL) mission, responsible for operating the Curiosity rover, and the Mars Exploration Rovers (MER) mission, which operated the Spirit and Opportunity rovers.

Below are examples of images taken by martian rovers with their labels. 

![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/41e1d8c0-5c3c-44b6-89e2-280b6914800c)
![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/51a9ec7d-1a21-4821-bb92-3285c9ff0657)


**Methodology:**

The repository includes a Python notebook for extracting, processing, and visualizing the AI4Mars dataset. You can find examples of loading random images, corresponding labels, and overlaying transparent masks to visualize terrain classification. The code is designed to work with the specific structure and format of the AI4Mars dataset. 
The neural network architecture choosen here is a U-net. Due to a lack of computing ressources, the input images were reduced to 128x128 instead of 1024x1024.

![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/4329316a-017b-47e0-bdd9-edf330993518)

The model was trained for 15 epochs with a batch size of 32, the loss function used was the crossentropy and the optimizer is adam. 


**Results:**
The model achieved a total accuracy of 84 % at the end of its training. 
The following confusion matrix was obtained :
![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/ac766671-03ab-43fc-a7f8-0b109fdc0c03)
We notice the low percentage of accurate predictions for the big rocks category. This is due to the low percentage of this label in the training dataset.

Below are good predictions on unseen images :
![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/fa53ddd7-ab70-4919-b5e8-c12c18d27a06)

**Possible improvements :** 

TBD
**Acknowledgments:**

This work is inspired by and based on the research presented in the paper "Deep Learning for Mars Rover Terrain Classification." by Brandon Rothrock, Jeremie Papon, Ryan Kennedy, Masahiro Ono, Matt Heverly. I acknowledge the California Institute of Technology and the contributors to the AI4Mars dataset. The dataset is publicly accessible at this link : https://data.nasa.gov/d/cykx-2qix
