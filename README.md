## This repository contains the code developed during the YData industrial project for Forter

The project aimed to implement a POC for a novel feature designed to enhance fraud ring detection. The concept was based on creating a semantic space of item names to group similar products regardless of naming variations, differentiate products with similar names but different underlying attributes. By adding existing and new features to this semantic space, the project demonstrated the ability to detect fraud rings that employ relatively stable product purchasing strategies.

To achieve this, solutions optimized for minimal computational resources were proposed:
* Transitioning from analyzing individual transactions to analyzing shopping carts.
* Generating item name embeddings using a lightweight spaCy model, preserving semantic distinctions.
* Introducing lag features representing the conditional probability of product appearances in baskets across specific online shops.
* Employing a CatBoost classification model, known for its speed and efficiency in handling categorical variables.
  
Despite these "lightweight" solutions, downsizing data during testing was necessary. Additionally, the project utilized the NVIDIA RAPIDS library to speed up the calculation of lag features in pandas, reducing computation and processing times significantly.

The repository includes notebooks with working code for data preprocessing and classification. However, for confidentiality reasons, the dataset is not provided. A brief overview of the project and its results can be found in the poster also available in this repository.
