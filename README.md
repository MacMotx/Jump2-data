# Jump_2_Digital 2022 

## Air quality classification 🌬

### Background 
The Paris Agreement is an international treaty on climate change that was adopted by 196 Parties at COP21 in Paris. Its goal is to limit global warming to well below 2, preferably 1.5 degrees Celsius, compared to pre-industrial levels.

To reach this long-term temperature goal, countries aim to peak greenhouse gas emissions as soon as possible to achieve a climate-neutral planet by mid-century.

That is why the European Union is allocating large amounts of resources to the development of new technologies that allow the improvement of the fight against pollution. One of these is a new type of sensor based on laser technology that allows air quality to be detected based on different sensors.


## Problem 🥅

The objective of the challenge will be to make a predictive model based on Random Forests that allows knowing the type of air quality based on the measurements of the sensors.

## The Data 💾

Features: The dataset contains 8 features in 8 columns, which are the parameters measured by the different sensors. These correspond to the different interactions that the laser beams have had when passing through the air particles.

Target: The target corresponds to the 'label' that classifies the quality of the air.

- Target 0 corresponds to Good air quality 
- Target 1 corresponds to Moderate air quality
- Target 2 corresponds to Dangerous air quality

## Analysis
Data exhibited near normal Distributions on all their features. Different transformations were tried separatedly on the test set (Standard Scaler, Power Transforms) just to see if It was a help for the ensemble learners but It didn't improve much of the linear models besides worsened practically all tested models.🤔 

## Results 
Random forest Classifier consistently was amongst the best results. Some other Algorithms that delivered the highest scores were the ensemble Voting Classifier and the KNeighbors Classifier. 

| **_Random Forest_** | precision | recall | f1-score | support |
|---------------------|-----------|--------|----------|---------|
| Good                | 0.9387    | 0.9087 | 0.9234   | 219     |
| Moderate            | 0.8904    | 0.9375 | 0.9133   | 208     |
| Toxic               | 0.8945    | 0.8768 | 0.8856   | 203     |
|                     |           |        |          |         |
| accuracy            |           |        | 0.9079   | 630     |
| macro avg           | 0.9079    | 0.9077 | 0.9075   | 630     |
| weighted avg        | 0.9085    | 0.9079 | 0.9079   | 630     |


| **_KNeighbors_** | precision | recall | f1-score | support |
|------------------|-----------|--------|----------|---------|
| Good             | 0.9398    | 0.9269 | 0.9333   | 219     |
| Moderate         | 0.9108    | 0.9327 | 0.9216   | 208     |
| Toxic            | 0.9104    | 0.9015 | 0.9059   | 203     |
|                  |           |        |          |         |
| accuracy         |           |        | 0.9206   | 630     |
| macro avg        | 0.9204    | 0.9204 | 0.9203   | 630     |
| weighted avg     | 0.9208    | 0.9206 | 0.9206   | 630     |


| **_Voting Ensemble_** | precision | recall | f1-score | support |
|-----------------------|-----------|--------|----------|---------|
| Good                  | 0.9263    | 0.9178 | 0.9220   | 219     |
| Moderate              | 0.8834    | 0.9471 | 0.9142   | 208     |
| Toxic                 | 0.9000    | 0.8424 | 0.8702   | 203     |
|                       |           |        |          |         |
| accuracy              |           |        | 0.9032   | 630     |
| macro avg             | 0.9032    | 0.9024 | 0.9021   | 630     |
| weighted avg          | 0.9037    | 0.9032 | 0.9027   | 630     |


## License
GPL (See LICENSE document)
