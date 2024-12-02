#This repository contains the code created and results obtained during the YData industrial project for Forter.

The project aimed to implement a Proof of Concept for a novel feature designed to enhance fraud ring detection. The concept was based on creating a semantic space of product names to:

Group similar products regardless of naming variations.
Differentiate products with similar names but different underlying attributes.
By adding existing and/or new features to this semantic space, the project demonstrated the ability to detect fraud rings that employ relatively stable product purchasing strategies.

To achieve this, the project proposed solutions optimized for minimal computational power:

Transitioning from analyzing individual transactions to analyzing product baskets.
Generating product name embeddings using a lightweight spaCy model, preserving semantic distinctions.
Introducing lag variables representing the conditional probability of product appearances in baskets across specific online stores.
Employing a CatBoost classification model, known for its speed and efficiency in handling categorical variables.
Despite these "lightweight" solutions, downsizing data during testing was necessary. Additionally, the project utilized the NVIDIA RAPIDS library to accelerate the calculation of lag variables in pandas, reducing computational requirements and cutting processing times by an order of magnitude.

The repository includes working code for data preprocessing and classification problem-solving. However, for confidentiality reasons, the dataset is not provided. A brief overview of the project and its results can be found in the poster available in this repository.
