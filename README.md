# Web_Mining_Project

A two-tower neural network model consists of two parallel subnetworks—one for users and one for products—each designed to learn latent representations from their respective feature sets. These embeddings capture user preferences and product characteristics in a shared vector space, enabling the model to predict interactions such as ratings or affinities.

*User Tower:

The user tower takes as input a rich set of features that reflect both user identity and behavior. These include unique identifiers like author_id, behavioral statistics such as average rating, number of reviews, and helpfulness score, as well as personal attributes like skin tone. Additionally, high-dimensional semantic information is provided through textual embeddings extracted from user-generated content, such as reviews. These features are processed through embedding and dense layers to produce a compact user embedding vector V_u that represents the user’s preferences.

*Product Tower:

The product tower receives features that describe the product’s properties and overall appeal. These include numeric attributes such as price, average rating, and number of reviews, as well as binary indicators of availability and exclusivity, such as whether the product is new, limited edition, or sold exclusively by the platform. Categorical product descriptors like type, formulation, and category (e.g., makeup, skincare) provide contextual detail, while brand frequency and size-related attributes help capture product scale and popularity. These inputs are also passed through appropriate preprocessing layers to produce the product embedding vector V_m.

Scoring:

The final prediction is computed as the dot product of the user and product embedding vectors:

score = V_u * V_m (dot product)

This scalar score reflects the compatibility between a given user and product and can be used for tasks like ranking, recommendation, or rating prediction. The two-tower architecture is particularly effective in large-scale recommendation systems, where it allows for efficient candidate generation and retrieval by separately encoding users and items.

**Additionally, this project included matrix factorization using SVD, as well as simple content-based and collaborative filtering approaches

Dataset:

https://www.kaggle.com/datasets/nadyinky/sephora-products-and-skincare-reviews/data  

•	product_info: stores product information  
•	reviews_0-250.csv: Contains reviews for products indexed from 0 to 250.  
•	reviews_250-500.csv: Contains reviews for products indexed from 250 to 500.  
•	reviews_500-750.csv: Contains reviews for products indexed from 500 to 750.  
•	reviews_750-1250.csv: Contains reviews for products indexed from 750 to 1250.  
•	reviews_1250-end.csv: Contains reviews for products indexed from 1250 to the last product in the dataset.  
