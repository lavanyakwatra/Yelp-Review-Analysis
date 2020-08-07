
YELP REVIEW ANALYSIS 

By Lavanya Kwatra

——————————————————————————————

SUMMARY:

This analysis is on the Yelp Review Dataset that is an open source database available for download on their website. Employing NLP on the review text to detect the sentiments of the reviews and thereby, classify the words that indicate positive and negative sentiments.

For an online review platform with user generated reviews, understanding the social perception of the business & review content through member interaction such as votes is a key consumer metric. 

——————————————————————————————


FOLDER STRUCTURE:

1. README.txt - Text file with instructions
2. Yelp S3 Bucket on AWS
3. Notebook 1 - Introduction & Data Selection
4. Notebook 2 - Data Sampling
5. Notebook 3 - EDA & Preprocessing
6. Notebook 4 - Modelling & Parameter Optimization
7. Conclusion & Results Report
8. Sample Datasets Folder - containing csv files.

——————————————————————————————

DESCRIPTION:

A. Yelp S3 Bucket on AWS:

I created an S3 bucket called “Yelp” on AWS to upload the data for quicker computation & filtering using a Sagemaker Notebook Instance. 

- This bucket contains 3 j.son files: business.json, user.json and review.json, that are downloaded from Yelp’s website.

Source: https://www.yelp.com/dataset
Documentation: https://www.yelp.com/dataset/documentation/main

- sample.csv : Generated from notebook 1, a sample of the main data frame created by concatenating the three .json files.

B. Jupyter Notebooks:

1. Introduction & Data Selection:

This notebook begins with defining the problem space & reading in all of the available data and taking a sample of it for exploration in the next notebook. This notebook was hosted on an AWS Sagemaker Notebook Instance and accesses the files in the Yelp S3 bucket.

2. Data Sampling:

This notebook uses the sample.csv created in the previous notebook and then filters to include only open restaurants & performs basic preprocessing steps on the data. This notebook was hosted on an AWS Sagemaker Notebook Instance and accesses the files in the Yelp S3 bucket.

3. EDA & Preprocessing:

This notebook uses a smaller sample of 10,000 reviews, with corresponding user & business data points, to show exploratory analysis, final preprocessing including text vectorization & feature engineering to prepare the dataset for modelling. This notebook was hosted on my local computer.

4. Modelling & Parameter Optimization:

This notebook includes the modelling & parameter optimization steps to evaluate the accuracy of classification.

C. Conclusion & Results Report:

A final conclusion of the results of my analysis along with next steps to improve our analysis & suggestions for Yelp.

D. Sample Datasets Folder:

- sample_yelp_df.csv = The main sample of 10,000 data points, with all corresponding review, business and user data, created in Notebook 2 and used in Notebook 3.

Apart from creating a main sample to use in our EDA & Modelling, I created 5 separate data frames in Notebook 2. This reorganization of the data structure could be useful for visualizations in Tableau at the next stage. 

sample_location.csv =  A sample of 10,000 data points for business location/address specifics of the businesses that are in the sample set. This can be used to plot businesses on a map since it contains the geographical coordinates. The aim is to use this to visualize consumer trends, grouped by business.

sample_business.csv =  A sample of 10,000 data points corresponding to the reviews in the main sample_yelp_df.csv, containing the business details & attributes. This can be used to explore the different restaurants & their features.

sample_review.csv = A sample of 10,000 data points of the reviews in the main sample_yelp_df.csv & it’s corresponding attributes. This includes the main independent feature, the review text written by the user, and the target feature which is the star rating given to the business by the user, for that corresponding review. It also includes other review attributes that we will explore to further understand the social perception of the business.

sample_social.csv = A sample of 10,000 data points corresponding to the reviews in the main sample_yelp_df.csv, with attributes relating to social features in the user community such as friends, fans, votes received by the user, etc. 

sample_user.csv = A sample of 10,000 data points corresponding to the reviews in the main sample_yelp_df.csv, with information about the user who wrote the review. This can be used to run a cluster analysis on our user community, thereby, identifying the best segmentation & targeting practices for Yelp & the businesses on Yelp, by taking users’ social perception into consideration while defining those clusters. 
 
——————————————————————————————

