# Self-Driving-Mars-Rover

**Introduction:**

This repository contains a neural network to classify pixels of images taken on the surface of Mars by rovers. It uses the AI4Mars dataset, a comprehensive collection designed for training and validating terrain classification models tailored for Mars rovers. The motivation behind this project stems from the observation that, while classical machine vision systems have been pivotal for Mars rovers, the integration of deep learning capabilities, such as semantic segmentation and object recognition, could significantly enhance safety and productivity during Mars missions.

The AI4Mars dataset comprises approximately 326,000 labeled semantic segmentation full image labels across 35,000 images captured by the Curiosity, Opportunity, and Spirit rovers. These images were meticulously labeled through crowdsourcing, involving around 10 contributors per image to ensure label quality and consensus. Additionally, the dataset includes 1,500 validation labels annotated by experts from NASA’s Mars Science Laboratory (MSL) mission, responsible for operating the Curiosity rover, and the Mars Exploration Rovers (MER) mission, which operated the Spirit and Opportunity rovers.

Below are examples of images taken by martian rovers with their labels. 

![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/41e1d8c0-5c3c-44b6-89e2-280b6914800c)
![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/51a9ec7d-1a21-4821-bb92-3285c9ff0657)


**Methodology:**

The repository includes a Python notebook for extracting, processing, and visualizing the AI4Mars dataset. Examples demonstrate loading random images, corresponding labels, and overlaying transparent masks to visualize terrain classification. The chosen neural network architecture is a U-net, and due to limited computing resources, input images were resized to 128x128 instead of 1024x1024.

![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/4329316a-017b-47e0-bdd9-edf330993518)

The model underwent training for 15 epochs with a batch size of 32. The loss function employed was cross-entropy, and the optimizer used was Adam.


**Results:**

The model achieved an overall accuracy of 84% after the completion of training. A confusion matrix was generated, highlighting challenges in accurately predicting the "big rocks" category, attributed to its low representation in the training dataset.

![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/ac766671-03ab-43fc-a7f8-0b109fdc0c03)

Examples of successful predictions on unseen images are displayed below:

![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/fa53ddd7-ab70-4919-b5e8-c12c18d27a06)
![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/95e25c81-2998-4021-84f4-2c948996f27f)
![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/ee409592-b872-45b2-8804-33d1b4cff608)
![image](https://github.com/AmauryPe/Self-Driving-Mars-Rover/assets/105310493/577f4312-62c9-472c-ad08-376783394a08)



**Possible improvements :** 

The confusion matrix highlights challenges in predicting the "big rock" label accurately, primarily due to its limited representation in the training dataset. Improving accuracy for sand labeling, crucial for rover navigation, is a key focus, and reward mechanisms for correct sand labeling could enhance results.

Comparison with the SPOCv2 model's architecture could provide insights into potential improvements. Reshaping images from 1024x1024 to 128x128 for training efficiency sacrifices spatial information; exploring model performance on original-sized images may yield better results.

Addressing label relevance concerns, especially in distinguishing bedrocks and soil, could enhance model interpretability.

**Next steps**

The ultimate goal of this terrain classification is to enable Martian rovers to navigate autonomously, reducing dependence on Earth-based commands with communication delays. Future steps involve integrating this terrain classification into a broader algorithm for optimal route planning based on specific objectives.

Feel free to explore, contribute, and join the journey of self-driving Mars rovers!

**Acknowledgments:**

This work is inspired by and based on the research presented in the paper "Deep Learning for Mars Rover Terrain Classification." by Brandon Rothrock, Jeremie Papon, Ryan Kennedy, Masahiro Ono, Matt Heverly. I acknowledge the California Institute of Technology and the contributors to the AI4Mars dataset. The dataset is publicly accessible at this link : https://data.nasa.gov/d/cykx-2qix
