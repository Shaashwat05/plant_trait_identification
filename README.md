# Plant Trait Identification

The project aims to identify physical traits in plants using images as input and identify if traits within plant species are being affected by external factors.

## Algorithm 

The approach to analyzing the dependency of external factors on plant traits is partially supervised and partially unsupervised. The backbone of this algorithm is a Resnet50V2 model fine-tuned on the plant image data similar to the work done by Schiller et al [1]. The input plant image is segmented using Facebook’s segment anything model, then the segmented images are used to train the Resnet with additional layers using Transfer learning. Finally, the model is used to generate latent vectors of size 2048, decomposed to 100 using PCA and clustered using K means clustering. 

## Workflow

![Project Workflow](https://github.com/Shaashwat05/plant_trait_identification/blob/main/Resources/Algorithm.png)

## Results

![Model Training](https://github.com/Shaashwat05/plant_trait_identification/blob/main/Resources/Model%20Training.png)

## File Descriptions

### data_handling - Downloading Images based on traits 

### model_from_directory - loading data and trainingthe model 

### segmenting_data - segmenting the download images for training 

### prediction - prediciting trait value and analyzing the predictions 

### milkweed_clustering - Clustering Milkweed Images 

### plant_trait_EDA - Data Analysis on the complete data 
