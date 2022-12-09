# Jump_2_Digital 2022 
![My Remote Image](https://www.rpsgroup.com/media/2484/air-quality-1600x1000.jpg?anchor=center&mode=crop&width=1200&height=630&rnd=131915165990000000)
## Air quality classification 🌬

### Background 
The Paris Agreement is an international treaty on climate change that was adopted by 196 Parties at COP21 in Paris. Its goal is to limit global warming to well below 2, preferably 1.5 degrees Celsius, compared to pre-industrial levels.

To reach this long-term temperature goal, countries aim to peak greenhouse gas emissions as soon as possible to achieve a climate-neutral planet by mid-century.

That is why the European Union is allocating large amounts of resources to the development of new technologies that allow the improvement of the fight against pollution. One of these is a new type of sensor based on laser technology that allows air quality to be detected based on different sensors.


## Goal 🥅

The objective of the challenge will be to make a predictive model based on Random Forests able to correctly classify the quality of the air based on the measurements of the laser sensors.


## The Data 💾

Features: The dataset contains 8 features in 8 columns, which are the parameters measured by the different sensors. These correspond to the different interactions that the laser beams have had when passing through the air particles.

Target: The target corresponds to the 'label' that classifies the quality of the air.

- Target 0 corresponds to Good air quality 
- Target 1 corresponds to Moderate air quality
- Target 2 corresponds to Dangerous air quality


## Analysis 🔍

Data exhibited near normal Distributions on all their features.Different transformations were tried separatedly on the test set (Standard Scaler, Power Transforms) after removing highly correlated features and non informatives.
This way we were able to see in place how models behave whith each train subset

The spot-check algorithms were a mixture of Linear, nonLinear and Ensemble Algorithms


## Results 💎

The Voting Classifier Method obtained the best results after slightly imbalancing the target. This helped the model to discern better Toxic/Moderate Air Quality labels and in turn slightly reduced their false negatives.  


| **_Voting Classifier_** | precision | recall | f1-score | support |
|-------------------------|-----------|--------|----------|---------|
| Good                    | 0.9437    | 0.9178 | 0.9306   | 219     |
| Moderate                | 0.9238    | 0.9327 | 0.9282   | 208     |
| Toxic                   | 0.9082    | 0.9261 | 0.9171   | 203     |
| accuracy                |           |        | **0.9254**| 630    |
| macro avg               | 0.9252    | 0.9255 | 0.9253   | 630     |
| weighted avg            | 0.9257    | 0.9254 | 0.9254   | 630     |


## License 
GPL (LICENSE.txt)
