# Self-Driving-Mars-Rover

Introduction: 

This repository contains a neural network to classify pixels of images taken on the surface of Mars by rovers. It uses the AI4Mars dataset, a comprehensive collection designed for training and validating terrain classification models tailored for Mars rovers. The motivation behind this project stems from the observation that, while classical machine vision systems have been pivotal for Mars rovers, the integration of deep learning capabilities, such as semantic segmentation and object recognition, could significantly enhance safety and productivity during Mars missions.

The AI4Mars dataset comprises approximately 326,000 labeled semantic segmentation full image labels across 35,000 images captured by the Curiosity, Opportunity, and Spirit rovers. These images were meticulously labeled through crowdsourcing, involving around 10 contributors per image to ensure label quality and consensus. Additionally, the dataset includes 1,500 validation labels annotated by experts from NASA’s Mars Science Laboratory (MSL) mission, responsible for operating the Curiosity rover, and the Mars Exploration Rovers (MER) mission, which operated the Spirit and Opportunity rovers.

Methodology:

The repository includes a Python notebook for extracting, processing, and visualizing the AI4Mars dataset. You can find examples of loading random images, corresponding labels, and overlaying transparent masks to visualize terrain classification. The code is designed to work with the specific structure and format of the AI4Mars dataset. 
The neural network architecture choosen here is a U-net. 

Results:
TBD

Acknowledgments:

This work is inspired by and based on the research presented in the paper "Deep Learning for Mars Rover Terrain Classification." by Brandon Rothrock, Jeremie Papon, Ryan Kennedy, Masahiro Ono, Matt Heverly. I acknowledge the California Institute of Technology and the contributors to the AI4Mars dataset. The dataset is publicly accessible at this link : https://data.nasa.gov/d/cykx-2qix
