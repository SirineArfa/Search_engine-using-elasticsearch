# Search_engine-using-elasticsearch
Image and text search_engine using elasticsearch and and Approximate nearest neighbors.

![thumbnail_1](https://user-images.githubusercontent.com/80635318/206896117-fbeb744e-9bbf-4af8-a666-bb25b2ead9b7.jpg)

# About the project
This academic project represents an image and text search engine that covers a 7200 image instance of OpenImages V6 which is a large scale dataset. We performed feature extraction from the images with VGG16 model to get a feature vector of length 4096 and then we reduced these dimentions to only 512 using a PCA-Principal Component Analysis of 512 components.
# Prerequisites

You must have the following Prerequisites:

 - ElasticSearch 7.14.1
 - Elastiknn plugin 7.14.1.0
 - kibana7.14.1.0
 - Python 3.9.6
 
# Pipeline :

Our project was composed of 3 main steps : 
  ###### Data preprocessing : 
  
 We performed feature extraction from the images with VGG16 model to get a feature vector of length 4096 and then we reduced these dimentions to only 512 using a PCA-Principal Component Analysis of 512 components.
 
 ###### Data indexing to Elasticsearch:
 
 The feature vectors of length 512 were all indexed to an Elasticsearch Index using ElasticSearch python client that uses Elastiknn plugin. We also indexed textual data in the same index.
 
 ###### Application development:
 
 To visualise how our model performed with image and text search a web application is developed using:
 
  - ElasticSearch python client: to query elasticsearch index.
  - Streamlit : to design a frontend for the application where users perform text and image search.
 
