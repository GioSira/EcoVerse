# EcoVerse: An Annotated Twitter Dataset for Eco-Relevance Classification, Environmental Impact Analysis, and Stance Detection

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

**Guidelines Availability**: We made the dataset annotation guidelines available upon request. Please feel free to request the annotation guidelines by writing to: fr.grasso@unito.it.

## Dataset Description

### Data Format
EcoVerse is distributed in compliance with Twitter Developer Terms: https://developer.twitter.com/en/developer-terms/more-on-restricted-use-cases
Note: Due to licensing restrictions, the dataset only provides **tweet IDs** and their annotations.Users must retrieve the original tweet text using the Twitter API.

The EcoVerse dataset is organized into five distinct folds, each serving a specific research need:

- `original`: Contains the annotations from Annotator I and Annotator II in JSON format.
- `clean_url_and_tag`: The dataset from Annotator II, divided into training, evaluation, and test sets with URLs and user mentions removed.
- `no_climatescam`: A version of `clean_url_and_tag` with the hashtag #climatescam removed.
- `no_environment`: A version of `clean_url_and_tag` without the hashtag #environment.
- `no_environment_no_climatescam`: The `clean_url_and_tag` dataset excluding both hashtags #environment and #climatescam.

### Field Descriptions
Each line in the JSON files has the following structure:

- **twitter_id**: The tweet ID, used to retrieve its content via the Twitter API.
- **annotator**: The ID of the annotator (1 or 2) who assigned the label
- **greenyesno**: Indicates whether the tweet is **Eco-related** or **Not eco-related**.
- **sentiment**: The environmental impact conveyed by the tweet (only for eco-related tweets)
- **stance**: The author's stance on the discussed environmental topic (only for eco-related tweets)

### Code
We provide a Jupyter notebook that contains the code to train and evaluate BERT-based models using the EcoVerse dataset. 
The models include, but are not limited to, ClimateBERT, and demonstrate the efficacy of the dataset in training models
specifically tailored for environmental texts.

## Citation
You can find the full paper in this repository under `EcoVerse.pdf`.

If you use EcoVerse in your research, please cite:

> Francesca Grasso, Stefano Locci, Giovanni Siragusa, and Luigi Di Caro. 2024. EcoVerse: An Annotated Twitter Dataset for Eco-Relevance Classification, Environmental Impact Analysis, and Stance Detection. In Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024), pages 5461–5472, Torino, Italia. ELRA and ICCL.

## License
EcoVerse © 2023 is licensed under the Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) license. This means you 
are free to share, copy, distribute, and transmit the work or to adapt it, provided you attribute it appropriately, 
and distribute any derivative works under a similar license.

For full license details, please refer to the `LICENSE.txt` file provided with the dataset.
