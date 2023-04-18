# Towards Climate Awareness in NLP Research
The environmental impact of AI, and particularly Natural Language Processing (NLP), has become significant and is worryingly increasing due to the enormous energy consumption of model training and deployment. Here, we draw on corporate climate reporting standards and proposes a model card for NLP models, aiming to increase reporting relevance, completeness, consistency, transparency, and accuracy.

This repository contains the code and model card templates accompanying the paper [Towards Climate Awareness in NLP Research](https://aclanthology.org/2022.emnlp-main.159/), presented in [EMNLP 2022](https://2022.emnlp.org/):

```
@inproceedings{hershcovich-etal-2022-towards,
    title = "Towards Climate Awareness in {NLP} Research",
    author = "Hershcovich, Daniel  and
      Webersinke, Nicolas  and
      Kraus, Mathias  and
      Bingler, Julia  and
      Leippold, Markus",
    booktitle = "Proceedings of the 2022 Conference on Empirical Methods in Natural Language Processing",
    month = dec,
    year = "2022",
    address = "Abu Dhabi, United Arab Emirates",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2022.emnlp-main.159",
    pages = "2480--2494",
    abstract = "The climate impact of AI, and NLP research in particular, has become a serious issue given the enormous amount of energy that is increasingly being used for training and running computational models. Consequently, increasing focus is placed on efficient NLP. However, this important initiative lacks simple guidelines that would allow for systematic climate reporting of NLP research. We argue that this deficiency is one of the reasons why very few publications in NLP report key figures that would allow a more thorough examination of environmental impact, and present a quantitative survey to demonstrate this. As a remedy, we propose a climate performance model card with the primary purpose of being practically usable with only limited information about experiments and the underlying computer hardware. We describe why this step is essential to increase awareness about the environmental impact of NLP research and, thereby, paving the way for more thorough discussions.",
}
```

## Getting Started
To fill the model card, you should answer the following questions:

1. _Is the resulting model publicly available?_ Yes or no. A popular model repository is [Hugging Face](https://huggingface.co/models).
2. _How much time does the training of the final model take?_ Training time for one model (the one that is publicaly available, if applicable). We recommend tools like [Weights & Biases](https://wandb.ai/) to track computations.
3. _How much time did all experiments take (incl. hyperparameter search)?_ Total time for all training runs of variations of that model.
4. _What was the energy consumption (GPU/CPU)?_ Also referred to as Max Thermal Design Power (TDP). Check your GPU specifications (example: [A100](https://www.nvidia.com/en-us/data-center/a100)).
5. _At which geo location were the computations performed?_ Country where the server or data center is located.
6. _What was the energy mix at the geo location?_ Find your country [here](https://lowcarbonpower.org/map-gCO2eq-kWh). The unit is gCO2eq/kWh.
7. _How much CO2eq was emitted to train the final model?_ Can be estimated after computations are done using tools such as the [ML CO2 Impact calculator](https://mlco2.github.io/impact/), but the eaiser and most accurate is using [CodeCarbon](https://codecarbon.io/) or [carbontracker](https://github.com/lfwa/carbontracker) while running the model training.
8. _How much CO2eq was emitted for all experiments?_ Total emissions for all training runs of variations of that model.
9. _What is the average CO2eq emission for the inference of one sample?_ With a trained model, estimate this for one instance/sentence/document, depending on what makes sense for your task.
10. _Which positive environmental impact can be expected from this work?_ Is it fundamental theory? Building block tool? Applicable tool? Deployed application? See [Jin et al. (2021)](https://aclanthology.org/2021.findings-acl.273/).

For a visual tutorial, see our [slides](emnlp2022-climate-awareness-nlp-slides.pdf), also presented at EMNLP 2022.


## Example Model Cards

The directory [`model_cards`](model_cards/) contains model cards for some commonly used NLP models, including [GPT-3](model_cards/gpt3.md) and [BLOOM](model_cards/bloom.md).

[Here](model_cards/climatebert.md) is an example climate performance model card according to the guidelines proposed in this paper. The model is [ClimateBert](https://climatebert.ai/), a language model finetuned on climate-related text. The same information is provided on the [Hugging Face model page](https://huggingface.co/climatebert).

<p align="center">
<img src="model_card_climatebert.png" width="400">
</p>

## Templates

[model_card_template.tex](model_card_template.tex) is a template that can be used in scientific papers to report the climate performance of models published along with them. The template can be included as part of a *Broader Impact* section. It requires the bibliography entry provided above. Authors are further encouraged to elaborate in the text on the accuracy of the provided information, possible improvements that can be done, and the positive environmental impact expected from their work.

[model_card_template.md](model_card_template.md) is a template that can be used in the model card on Hugging Face, for example, to report the climate performance of the model.

## Survey of Climate Discussion in NLP

[Towards_Climate_Awareness.ipynb](Towards_Climate_Awareness.ipynb) is a collaborative notebook with the code used to conduct our survey of 2016-2022 papers from the [ACL Anthology](https://aclanthology.org/).
The following figure from the paper visualizes the development of proportions of deep-learning-related *ACL papers discussing *public* model weights, *duration* of model training or optimization, *energy* consumption, *location* where computations where performed, and *emission* of GHG.

<p align="center">
<img src="survey_proportions.png" width="400">
</p>

## See Also
[It's Easy Being Green in Machine Learning](https://dustinwright.substack.com/p/its-easy-being-green-in-machine-learning?publication_id=1395146&post_id=115560251), blog post by Dustin Wright. 
