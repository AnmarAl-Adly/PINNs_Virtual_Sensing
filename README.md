# PINNs_Virtual_Sensing
This repository presents open-access code for developing Physics-Informed Neural Networks for virtual sensing in beams subjected to moving loads, as demonstrated in the case studies of a research paper.

Physics-informed neural networks (PINNs) show promise for structural health monitoring and related applications since they have the potential to represent physical systems and processes by conforming to governing differential equations as well as physical constraints such as displacement and force boundary conditions. This paper addresses the challenge of developing PINNs that can predict the response of bridge structures under a moving concentrated load such as from the axle load for a vehicle. It also demonstrates the potential of PINNs for virtual sensing, i.e., predicting response parameters at locations where sensors may not be available. The proposed PINNs assume that the load moves at constant speed and uses the time at which the load enters the bridge to evaluate its position with respect to time. The study initially proposes a one-dimensional PINN that takes only response location as input and gradually increases dimensionality (number of inputs) to three by including the vehicle passage time and load magnitude as additional inputs. The study conducts a thorough sensitivity analysis of the PINN model's parameters to understand their influence on model training and performance. The performance of the final PINN model is investigated for a real-world bridge girder for which monitoring data is available. The capacity of the PINN to predict strains, deflections and internal forces in locations that are not physically equipped with sensors is demonstrated, and strain predictions are observed to closely follow actual measurements from field monitoring.

## Development of PINNs
![alt text](https://github.com/AnmarAl-Adly/PINNs_Virtual_Sensing/blob/main/Figures/Fig.1.png)
Case Study 1 Schematic of Physics-Informed Neural Networks (PINNs).
![alt text](https://github.com/AnmarAl-Adly/PINNs_Virtual_Sensing/blob/main/Figures/Fig.2.png)
Case Study 2 Schematic of Physics-Informed Neural Networks (PINNs).

## Summary of Case Studies

| Case Study Number   | PINNs Inputs                          | PINNs Outputs                                | Loss Functions Terms    | Code Source                 |
|---------------------|---------------------------------------|----------------------------------------------|---------------------------------------------|-----------------------------|
| Case_study_1        | Spatial and temporal domains          | Predicted deflection and internal forces     | $$MSE_{\text{f}} + MSE_{\text{ic}} + MSE_{\text{bc}}$$ | [Go to the case study 1](Case_Study_1)|
| Case_study_2        | Spatial, temporal, and axle load domains | Predicted deflection and internal forces  | $$MSE_{\text{f}} + MSE_{\text{ic}} + MSE_{\text{bc}}$$ |  [Go to the case study 2](Case_Study_2)    |
| Case_study_3        | Spatial, temporal domains, and sensor data | Predicted deflection and strain-time history diagram | $$MSE_{\text{f}} + MSE_{\text{ic}} + MSE_{\text{bd}} + MSE_{\text{data}}$$ | [Go to the case study 3](Case_Study_3)  |
