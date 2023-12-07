# Trip purpose forecasting model for optimal energy management of electric vehicles supply equipment

## Overview

### The growing popularity of electric vehicles (EVs) and plug-in hybrid EVs has led to concerns about uncoordinated charging behaviors causing challenges in the power grid. These challenges include power quality degradation, increased operational costs, and impacts on the distribution network. Scheduling EV charging is crucial due to the unpredictability of user behaviors and the limitations in power supply for EV charging equipment. In a city setting, different types of EVs have varying charging needs, with household EVs often lacking private charging posts. The scheduling problem introduces uncertainties related to start time, stay duration, and energy demand, which cannot be entirely addressed through deterministic formulations. Machine learning approaches, particularly using decision trees, have shown promise in forecasting trip purposes for EVs entering charging stations, and this project aims to develop a trip purpose forecasting model based on an origin-destination dataset for enhanced energy management.

## Dataset

### The dataset utilized is the 2017 National Household Travel Survey (NHTS), offering a comprehensive view of transportation behaviors in the United States, with approximately 923,500 vehicle trips. The dataset covers various transportation-related variables, including trip durations, distances, and purposes. Notably, the dataset categorizes household EV trips into nine classes, providing granularity for the analysis.

## Models and Evaluation

### The study employs three machine learning models – linear models (Logistic Regression and LinearSVC), random forest, and a neural network – to address the classification problem of predicting trip purposes for electric vehicles (EVs) entering charging stations. Linear models serve as baseline models, capturing linear relationships, while random forest and neural network models handle non-linear relationships and intricate patterns in the data. The models are evaluated using classification metrics such as accuracy, precision, recall, and F1 score, with cross-validation ensuring robust evaluation

## Results

### Preprocessing steps include imputation for missing data, feature scaling, and one-hot encoding for categorical variables. Logistic Regression and LinearSVC baseline models yield results of 59% and 56% accuracy, respectively, on testing data. Random forest, after refinement steps, achieves a final accuracy of around 72%, with notable strength in predicting majority trip categories. The neural network model, using default hyperparameters, achieves an accuracy of 67%, with potential for further improvement through fine-tuning. Therefore, the best predictive model discovered was a 100 tree random forest with an accuracy of 72%. It was especially good at predicting results from the majority categories of home, shopping/errands, and work with an accuracy of nearly 85% in these three categories.

## Limitations

### The current model and report is simply a test of the predictive capabilities of a model trained in trip purpose predictions and how that prediction could be useful to the EV industry. However, applying this to the real-world would have many issues. One major problem is the reduction in real-world data and knowledge at the time of EV charging in order to predict the trip purpose and therefore optimize the charging of EVs at a charging station. The trip data used here is taken after the trip and has more available data, such as the start and end time of the trip, which is then used in our models for the prediction. To apply this to a real-world scenario would be much more difficult since we would have other, different features to work off of. This data could come from the EV itself, the user’s history, or other sources. Despite these limitations, such a model could be possible and, if implemented correctly, could provide major benefits to the rising industry of the electrification of transportation.

## Future Work

### Building on the current project's foundation, the next steps involve developing a comprehensive predictive framework for estimating the stay duration of EVs at EVSE locations. Leveraging the insights gained from predicting trip purposes using the NHTS dataset, future work entails integrating features from various datasets, including electrical utilities, and user feedback. Advanced machine learning techniques, such as reinforcement learning and time-series analysis, will be explored to capture temporal aspects and optimize dynamic charging infrastructure. The scalability and generalizability of the model will be a focus, ensuring its applicability across diverse geographic regions. The envisioned future work aims to contribute to a smarter and more responsive charging infrastructure, ultimately fostering the widespread adoption of EVs.

