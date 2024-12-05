# Predicting Clothing Fit From Customer Reviews on Rent the Runway Dataset
![1147849779](https://github.com/user-attachments/assets/578646c5-aff1-4793-a8cc-51604f0b44cd)


This project is focused on predicting clothing fit using NLP techniques applied to customer reviews.

The dataset can be accessed at [Kaggle](https://www.kaggle.com/datasets/pypiahmad/clothing-fit-data?select=renttherunway_final_data.json).

Rent the Runway is an online platform that allows users to rent, subscribe to, or buy designer clothing and accessories.

Online retail, especially Rent the Runway, faces challenges with sizing inconsistencies, which can lead to customer frustration and costly returns. Our solution uses advanced natural language processing methods to improve size recommendations, reduce returns, and enhance overall customer satisfaction.

However, inconsistent sizing feedback from customers poses a significant challenge. 
These discrepancies cause confusion and operational inefficiencies. This project seeks to address the fit challenge by analyzing customer reviews to classify items into fit categories, ensuring customers have a clearer idea of how an item will fit before renting. By addressing this problem, Rent the Runway can better serve its customers while reducing the operational burden of returns.

*************

**Dataset Overview**
Our dataset comes from Rent the Runway and includes 192,000 customer reviews labeled into fit categories. The feedback is available as structured information, and in form of a feedback statement in natural text.

*************
**TF-IDF and Logistic Regression**
We started with a traditional approach using TF-IDF. This method transforms text into numerical features based on word frequency and rarity, highlighting terms like “tight” and “baggy” that are critical for predicting fit issues.
Logistic Regression, a simple and interpretable linear model, was trained on these features. This combination of TF-IDF and Logistic Regression proved accurate, scalable, and well-suited to the dataset’s structure.

**Embeddings and BERT**
We also explored advanced techniques like embeddings and BERT. Embeddings convert words into dense numeric vectors, capturing semantic relationships and contextual meaning. BERT, in particular, is a state-of-the-art NLP model that processes text bidirectionally to understand the relationships between words.
For example, BERT can distinguish between “tight shoulders” and “tight hips,” making it highly effective for analyzing fit-specific feedback. However, while powerful, BERT’s computational cost and complexity make it less practical for this relatively straightforward task. Simpler methods like TF-IDF paired with Logistic Regression proved more efficient and equally effective in our case.

************
**Results and Insights**
Our best-performing approach combined TF-IDF with Logistic Regression, achieving a weighted F1 score of 0.79 and an accuracy of 81%. This indicates the model is reliable for predicting the dominant “Fit” category but struggled with the minority categories, “Small” and “Large,” due to dataset imbalance.
