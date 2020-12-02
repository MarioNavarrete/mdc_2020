# mdc_2020

This repository contains the Notebooks that generate the final recommendations that allowed me to belong to the top 10 participant on the Meli Data Challenge 2020.

Due the small local instance that I have in home, I was unable to generate a more robust code, but it was enough to produce results that are aligned with the requirements that the competition requests.

## Notebooks

In the repo you will find 3 different notebooks, that toghether, reproduce the steps that I had to do in order to produce my final recommendations (score between 0.283 - 0.284).

* __item_encoder__: This notebook generates Embeddings for all the items that appears in the items dataset.
* __predict_model__: This notebook generate the initial recommendation. This is the first step on the process. The main goal of this notebook was generate a Business Logic algorithm, powered by Machine Learning ideas (like *item-to-item* recommendation Matrix) and the usage of embeddings to fill some gaps in the recommendations. You will find some functions that has some pre-defined values for their parameters. This values were assigned after an exhaustive grid search of them, and also, the final logic configuration was the best of many other that were tested during the competition.
* __calibrate_results__: Given the recommendations provided in *predict_model.ipynb*, I use this second notebook to fill some gaps in the original recommendations (mostly filling with the most relevant domain in the first recommendation). This "calibration" process, provide an upgrade about 0.003 in the final score. It also contain some functions with parameters already defined after a large gridsearch over those ones.

If you follow this steps in order, you *should* be able to generate the final results. The notebooks shows the process and results using the training dataset. For producing the final recommendations, you will need to use the trainning without splitting it, and then, generate the recommendations using the rows of the test dataset.

This process is very basic, but is capable of provide good results using business logic, so, it's really easy to explain to non analytic people about how is working.
