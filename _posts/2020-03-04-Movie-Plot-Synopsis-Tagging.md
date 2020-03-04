---
published: true
---
![intro]({{ "/assets/img/mpst/image.jpg" | relative_url}})

### Introduction:

Social Tagging of movies reveals a wide range of heterogeneous information about movies, like the genre, plot structure, soundtracks, metadata, visual and emotional experiences. Such information can be valuable in building automatic systems to create tags for movies. Automatic tagging systems can help recommendation engines to improve the retrieval of similar movies as well as help viewers to know what to expect from a movie in advance. 

In this case study, we are using MPST dataset of 14k movie plot synopses which has 71 tagset describing multi-label association with synopses. The dataset is hosted by cryptexcode in kaggle datasets page is [here](https://www.kaggle.com/cryptexcode/mpst-movie-plot-synopses-with-tags) and the paper related to the dataset is [here](https://www.aclweb.org/anthology/L18-1274).

### Problem Statement:

Suggest the tags based on the plot synopses of the given movies.

### Dataset:

Contains IMDB id, title, plot synopsis, tags for the movies. There are 14,828 movies' data in total. The split column indicates where the data instance resides in the Train/Dev/Test split.

![image2]({{ "/assets/img/mpst/image2.jpg" | relative_url}})


### Real world Objectives and Constraints:
- Predict as many tags as possible with high precision and recall.
- Incorrect tags could impact movie search results generated based on tags.
- No strict latency constraints.

### Mapping the problem to Machine Learning problem:

##### Type of Machine Learning Problem:
It is a multi-label classification problem
Multi-label Classification: Multilabel classification assigns to each sample a set of target labels. This can be thought as predicting properties of a data-point that are not mutually exclusive, such as topics that are relevant for a document. A movie on MPST dataset might be about any of horror, comedy, romantic etc. at the same time or none of these.

### Performance Metric:

Micro-Averaged F1-Score (Mean F Score) : The F1 score can be interpreted as a weighted average of the precision and recall, where an F1 score reaches its best value at 1 and worst score at 0. The relative contribution of precision and recall to the F1 score are equal. 

![map]({{ "/assets/img/mpst/map.jpg" | relative_url}})
![mar]({{ "/assets/img/mpst/mar.jpg" | relative_url}})
![maf]({{ "/assets/img/mpst/maf.jpg" | relative_url}})

### Exploratory Data Analysis:
First, we have to check for any NaN or null entries and remove the duplicate rows.
##### Distrubution of Tags:

![tag_dist]({{ "/assets/img/mpst/tag_dist.jpg" | relative_url}})























