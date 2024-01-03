# final-project-python-mushroom

**Introduction**

Mushrooms are a diverse and fascinating group of organisms that can be found in a wide variety of habitats. They can be edible, toxic, or even psychoactive. It can be challenging to determine whether a mushroom is edible or toxic without specialized knowledge. Indeed, it is crucial to assess the toxicity of mushrooms before consuming them. Currently, there is a list of 140,000 documented mushroom species, making it difficult to recognize each variety. Distinguishing between toxic and non-toxic mushrooms can be a risky task, so it is the responsibility of our project to address this. 

 
**Existing Solutions**

There are a number of existing applications that can be used to identify mushrooms. However, these applications typically focus on identifying the species of mushroom. This is a challenging task, as there are many factors that can affect the appearance of a mushroom, including its maturity, odor, season, and environment. As a result, these applications can often provide inaccurate or incomplete identifications. 

 **Our Approach**

Our approach to mushroom identification is different from existing applications. We focus on identifying whether a mushroom is edible or toxic, rather than the species of mushroom. This approach is more accurate and reliable, as it is less affected by the factors that can change the appearance of a mushroom. 

**How can one determine the toxicity or edibility of a mushroom based on a simple photo of its physical characteristics ?**

We achieve this by using a deep learning model that is trained on a dataset of images of edible and toxic mushrooms. The model learns to identify the features that distinguish edible mushrooms from toxic mushrooms. This allows the model to accurately identify mushrooms, even if they are not in their ideal condition.

We aim to help users visually distinguish the differences and similarities between an edible mushroom and a toxic one by a binary method. 
The application will provide a toxicity percentage for the collected mushroom.

**WHY?** 
The ability to quickly and accurately identify mushrooms is important, especially in the wilderness. If you are lost or stranded in the wilderness, it is important to be able to find food. However, you also need to be able to identify edible mushrooms and avoid toxic mushrooms. 



**The diferent steps in our project :**

1. find a dataset of mushroom in "Mushroom world"
2. scrap information about species, edibility (binary classify as 0=eadible and 1=poisonous) and the link to the images
3. create fake images to have a large sample
4. fetch images from URL in dataframe -> convert the images to base 64 and encode it to put in a list
5. training the model with x_train and y_train
6. use a three_layered sequential model with a last outer layer of Sigmoid (binary)
7. compile the model with Adam model
8. predict with an image from the dataset given and add a precision rate to know the eadibility

   
**The problems encountered in our project :**

1. with our dataset, we only had 6000 images so we had to modify theses images by the zoom, rotation and create more and more of images to have a better result with our IA during the CNN. 
2. Large size for all images during encoding
3. Difficulty using the JSON, which was in the wrong format for loading (HTML <a> tags)
4. Images stored in JSON as lists of URLs, so it was necessary to remove the lists and transform the URLs into encoded images in string format using Base64.
5. Recreate the JSON data manually because the labels we needed were no longer present in the dataset (Information not available) on the edibility of all mushroom species. Therefore, we had to search for the edibility of each mushroom in the dataset, mark it in our JSON, and replace the missing information.
6. Have a sequential model that works and, during training, provides meaningful results. The initial results considered too much of the dataset, leading to no improvement in accuracy over epochs and an increase in loss. It was necessary to reduce the number of layers and the complexity of our AI.


