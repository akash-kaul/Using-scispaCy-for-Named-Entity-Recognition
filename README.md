# Using-scispaCy-for-Named-Entity-Recognition
### *A step-by-step guide to extracting data from biomedical literature*

This code walks you through the installation and usage of scispaCy for natural language processing. For our example, we use data from CORD-19, a large collection of articles about the Covid-19 pandemic.

# Motivation
scispaCy is a full, open-source spaCy pipeline for Python designed for analyzing biomedical and scientific text. It is a very powerful tool, especially for named entity recognition (NER), but it can be somewhat confusing to understand. The goal of this code is to show scispaCy in easy to understand terms. I hope it makes navigating the world of entity extraction a little easier.

# Layout
The code is divided into 5 main sections
1. Installing the necessary packages
2. Importing the packages
3. Reading a single text file
4. Reading in lots of data
5. Methods to help read in data

# 1. Installing the necessary packages
This part is pretty straightforward. We install scispacy and spacy along with the specific NLP models available in scispacy. The models are installed using their URLs, found [here](https://allenai.github.io/scispacy/).

# 2. Importing the packages
Importing these packages is the same as any other Python packages. Nothing new here.

# 3. Reading in a single text file
We use pandas to read in the csv file we want. All we need is the path to the file. Once that is done, we pick a specific text to extract from that file and pass it through one of the models. Then, we display our results.

## Example text before NER:
![sample text](https://miro.medium.com/max/1400/0*-yIISPSoS84zo3Qf)

## Text after NER
![sample text](https://miro.medium.com/max/1400/0*7ZkApBCraBd2JLIp)

# 4. Reading in multiple text files
This section expands the previous code to loop over the entire csv file and continually grab the text we want and use NER to grab the entities and their attributes.

# 5. Helper Methods
The helper methods are optional, but like all methods they help make the code a little more concise. The first 4, labeled "Methods to add entity/value pairs to table" each employ a different scispaCy model to add entities to the target table. The last method, labeled "Method to Extract Entity/Value Pairs" employs a given scispaCy model to perform entity extraction on a given text.

## Example Helper Method

![image4](https://user-images.githubusercontent.com/46678528/82264711-0e40e980-992b-11ea-928e-4ea3b9a9f4c6.png)

If you perform everything correctly, you should get your entity/value pairs along with the article doi in a nice looking CSV file. 

![image5](https://user-images.githubusercontent.com/46678528/82264986-92936c80-992b-11ea-8501-fe00af31f896.png)


If you're looking for more detailed instructions, check out the post I wrote about this code [here](https://medium.com/@akkukaul007/using-scispacy-for-named-entity-recognition-785389e7918d).
