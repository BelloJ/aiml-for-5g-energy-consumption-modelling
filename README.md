# AIML for 5G Energy Consumption Modelling

This repository contains a Jupyter notebook for modeling energy consumption in 5G networks using Artificial Intelligence and Machine Learning (AI/ML) techniques. It also contains the data sets that are required to sucessfully execute the notebook.


## Project Description

5G, the fifth generation of radio technology, has brought about new services, technologies, and networking paradigms, with corresponding social benefits. However, there is growing concern over the energy consumption of these new network deployments. While 5G networks are estimated to be about 4x more energy-efficient than 4G networks, their energy consumption is approximately 3x larger due to the need for a larger number of cells to provide the same coverage at higher frequencies and the increased processing required for wider bandwidths and more antennas.

Network operational expenditure (OPEX) already accounts for around 25 percent of the total operator’s cost, and 90 percent of it is spent on large energy bills. More than 70 percent of this energy is estimated to be consumed by the radio access network (RAN), particularly by the base stations (BSs), while data centres and fibre transport account for a smaller share.

Base station energy consumption depends on multiple factors, such as specific architecture (e.g. RRU or AAU), configuration parameters (e.g., number of operated carriers, bandwidth, transmit power), traffic conditions (e.g., number of allocated physical resource blocks), and the activation of energy-saving methods (e.g., symbol shutdown, RF shutdown). To reduce network energy consumption, it is crucial to optimize base station parameters and energy-saving methods. This requires a deep understanding of how these parameters and methods impact the energy consumption of different base stations. Therefore, accurate modelling of energy consumption is essential for achieving more energy-efficient network deployments.

This ML challenge targets addressing the important questions mentioned above. In the challenge, the participants are asked to design a machine learning-based solution that can be trained on a dataset of a few scenarios and then generalize successfully to data from scenarios not seen before. In particular, the designed machine learning model must be able to achieve the objectives stated herein.

### Objective A
Develop a model able to estimate the energy consumed by different base station products. The participants are required to develop a model that estimates the energy consumed by different base station products, taking into consideration the impact of various engineering configurations, traffic conditions, and energy-saving methods.

### Objective B
Achieve generalization capabilities across different base station products. The model must estimate the energy consumption of a new base station product based on measurements collected from existing ones, such as Products A, B, and C. For example, if training data is available for these three products, the model must be able to provide an estimate of the energy consumed by Product D.

### Objective C
Achieve generalization capabilities across different base station configurations. The model must predict the energy consumption of newly configured parameters based on a small number of real network configuration parameters. For instance, if the training data contains samples collected from many base station products when the transmit power is set to 30, 35, and 43 dBm, the model must estimate the energy consumed when the transmit power is set to 40 dBm.

### About AI for Good - International Telecommunication Union (ITU)
AI for Good is organized by ITU in partnership with 40 UN Sister Agencies. The goal of AI for Good is to identify practical applications of AI to advance the United Nations Sustainable Development Goals and scale those solutions for global impact. It’s the leading action-oriented, global & inclusive United Nations platform on AI.

### Evaluation
While the challenge is running, your submissions will be scored on Mean Absolute Error. For every row in the dataset, submission files should contain 2 columns: Time and Energy.

Your submission file should look like this (numbers to show format only):
```
Time              Energy
2023-01-01_B_0    84.154     
2023-01-01_B_0    17.178 
```
Once the challenge has closed, the private leaderboard will be delayed by 48 hours as we take your submission file and score it against WMAPE, and this will constitute your final leaderboard score. The private leaderboard scores of your two chosen submissions will be overwritten with your WMAPE scores, so remember to select your two best submissions before the deadline.

To focus on the cross-equipment and cross-configuration generalization capability of the model, the test set estimation accuracy is evaluated by using a weighted relative error evaluation method. Specifically, the error weight, \( w_i \), of the sample corresponding to the new device and/or new configuration in the test set is larger and is provided in the test set. The error metric is defined as:

\[\text{WMAPE} = \frac{\sum_{i=1}^{n} w_i | y_i - \hat{y_i} |}{\sum_{i=1}^{n} w_i | y_i |}\]


The final model performance is ranked according to the minimum WMAPE error.

Participants are required to submit:
- A CSV file named `power_consumption_prediction.csv`, containing the power consumption prediction performed over the test set;
- The developed model code;
- A report explaining their solution, including the outcomes of their models.

In evaluating the final submission, both the quality of the report (weighted 50%) and the achieved model score (weighted 50%) will be considered.

## Libraries Used

- scikit-learn
- google-colab
- pandas
- hyperopt
- numpy

## Installation

You can install the required libraries using pip:

```
pip install scikit-learn google-colab pandas hyperopt numpy
```

## Usage

To run the notebook, open it in a Jupyter notebook environment or in Google Colab. Make sure to install all the required libraries before running the notebook.

