# Customer Segmentation using ML
This repository contains a machine learning project focused on customer segmentation using the KMeans clustering algorithm. The project uses the popular Mall Customer Segmentation dataset, which includes basic demographic and behavioral data collected from customers via mall membership cards. The aim is to group customers into distinct clusters based on shared characteristics, enabling businesses to better understand customer types and design targeted marketing strategies.

# 📌 Task
The objective of this task is to segment mall customers using unsupervised machine learning, specifically KMeans clustering. The segmentation is based on the following features: Age, Gender, Annual Income (k$), and Spending Score (1–100). These features provide a good representation of both the demographic and behavioral aspects of each customer. The ultimate goal is to identify customer groups that share similar purchasing behaviors and income levels so that the business can create tailored strategies for each segment.

# 🧹 Data Preparation
The dataset was first loaded using the Pandas library. It consists of 200 rows and 5 columns: Customer ID, Gender, Age, Annual Income, and Spending Score. Since clustering does not require labels, only the relevant features —
Age

Gender

Annual Income

Spending Score

were selected for the analysis. The CustomerID column was dropped as it does not contribute to customer characteristics.

The data was checked for missing or duplicate entries, and none were found. The categorical feature Gender was converted into numerical format using label encoding, mapping "Male" to 0 and "Female" to 1. Numerical features such as Age, Income, and Spending Score were then scaled using StandardScaler to normalize the values, ensuring that each feature contributed equally to the clustering algorithm.

# 🤖 Model Training
Once the data was preprocessed, the Elbow Method was used to determine the optimal number of clusters. This technique involves plotting the Within-Cluster Sum of Squares (WCSS) against different values of k (number of clusters). The "elbow" point in the plot indicates the best number of clusters that balances model complexity and accuracy. Based on this analysis, the optimal number of clusters was selected.

The KMeans algorithm from Scikit-learn was then applied to the scaled data with the chosen number of clusters. Each customer was assigned a cluster label representing the group they belong to. The clustering results were visualized using 2D scatter plots, allowing for easy interpretation of how customers were grouped. Colors were used to distinguish clusters, and axes represented combinations of features such as Annual Income vs Spending Score or Age vs Spending Score.

# 📈 Results and Insights
The clustering revealed several distinct customer segments. For instance, some groups consisted of high-income, high-spending customers who are ideal candidates for premium product promotions. Others included low-income, low-spending customers, who might be less responsive to marketing campaigns and may require a different approach. There were also clusters of young customers with moderate income but high spending scores, who could be valuable targets for loyalty programs or seasonal offers.

By identifying these patterns, the mall can optimize its marketing strategies and customer relationship management efforts. Understanding which groups are most likely to respond to promotions helps reduce marketing costs while improving customer satisfaction and revenue. Additionally, the results provide business intelligence that could guide product placement, personalized offers, and customer service improvements.

# ✅ Conclusion
This project demonstrates how unsupervised learning, particularly KMeans clustering, can be effectively used to perform customer segmentation. By analyzing only a few basic attributes — age, gender, annual income, and spending score — we were able to extract meaningful insights into customer behavior. These insights can be leveraged to improve business decision-making and develop customer-focused strategies. The project also showcases the power of data science in solving real-world business problems using simple yet powerful machine learning techniques.
