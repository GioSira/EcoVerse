# EcoVerse: An Annotated Twitter Dataset for Eco-Relevance Classification

## Introduction
EcoVerse is a comprehensive annotated English Twitter dataset, consisting of 3,023 tweets, curated to advance research 
in eco-relevance classification, environmental impact analysis, and stance detection. This dataset stems from an urgent 
need to address anthropogenic ecological crises—a significant challenge confronting the academy, including the Natural 
Language Processing (NLP) community. While climate change discourse has been the center of attention, it's crucial 
to explore other environmental and ecological topics that are equally important but remain largely unaddressed.

EcoVerse aims to bridge this gap by providing a unique dataset that encompasses a wide range of environmental topics 
such as biodiversity loss, sustainable farming, and renewable energy. The data has been annotated with a novel 
three-level scheme designed to classify tweets based on their eco-relevance, analyze the environmental impact of 
the events or behaviors they discuss, and detect the author's stance towards these topics. The dataset encourages 
the development of NLP models that can better understand and analyze ecological narratives, thus supporting 
policy-making and public awareness efforts.

## Dataset Description

### Data Format
The EcoVerse dataset is organized into five distinct folds, each serving a specific research need:

- `original`: Contains the annotations from Annotator I and Annotator II in JSON format.
- `clean_url_and_tag`: The dataset from Annotator II, divided into training, evaluation, and test sets with URLs and user mentions removed.
- `no_climatescam`: A version of `clean_url_and_tag` with the hashtag #climatescam removed.
- `no_environment`: A version of `clean_url_and_tag` without the hashtag #environment.
- `no_environment_no_climatescam`: The `clean_url_and_tag` dataset excluding both hashtags #environment and #climatescam.

Data are organized as required by https://developer.twitter.com/en/developer-terms/more-on-restricted-use-cases

Each line in the JSON files has the following structure:

- **twitter_id**: The unique identifier for the tweet as assigned by Twitter.
- **id**: An internal unique identifier for the annotated tweet within the dataset.
- **greenyesno**: A label indicating whether the tweet is eco-related or not. Possible values include "Eco-related" and "Not eco-related".
- **sentiment**: The sentiment expressed in the tweet. This field is null if the tweet is not eco-related.
- **stance**: The stance of the tweet regarding the environmental topic discussed. This field is null if the tweet is not eco-related.

### Code
We provide a Jupyter notebook that contains the code to train and evaluate BERT-based models using the EcoVerse dataset. 
The models include, but are not limited to, ClimateBERT, and demonstrate the efficacy of the dataset in training models
specifically tailored for environmental texts.

## License
EcoVerse © 2023 is licensed under the Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) license. This means you 
are free to share, copy, distribute, and transmit the work or to adapt it, provided you attribute it appropriately, 
and distribute any derivative works under a similar license.

For full license details, please refer to the `LICENSE.txt` file provided with the dataset.
