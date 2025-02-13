# Medical Image Captioning for Chest X-rays

Medical Image captioning on chest X-rays for ELTE data mining course.

## Intoduction

Computational image tagging (also known as labeling)  is the process of providing a computer an unlabeled image and receiving metadata about that image in the form of a full piece of writing that in some way describes the contents of the image capturing some meaningful and human interpretable information about it.

Modern image captioning algorithms are not If, Else ... ‘classical’ algorithms but instead trained neural networks. Neural networks have been shown to perform well on this task (Karpathy and Fei-Fei 2015, 1) and are currently providing state of the art solutions for this problem. This success can be attributed to the capturing of high level visual features that have semantic meaning and the recent progress in the field of natural language processing (NLP), specifically in generative tasks like creating meaningful sentences i.e sequence generation.

## Goals

This project will loosely follow the article Medical Image Captioning on Chest X-Rays by (Chempolil 2021). The aim here is to recreate some of the results, explain choices in data cleaning and model as well as give an intuition into the field of image tagging's current state as well as its shortcomings. 

Specifically this study will compare two models. The first will contain an encoder decoder recurrent neural network that will be initialized with pre trained weights. The second will be a global attention model. The goal of the project will be to evaluate  both models and observe the advantages of the global attention network for a medical image tagging task.

## Reasults

Enoder decoder:

| Evaluation method | bleu1 | bleu2  | bleu3 | bleu4 |
| ------------- | ------------- | ------------- | ------------- | ----------- |
| Greedy search  | 0.107364 | 0.05736  | 0.0333 | 0.01467 |
| Beam search  | 0.11906  | 0.045302  | 0.020128  | 0.005991 |


Attention mechanism:

| Evaluation method | bleu1 | bleu2  | bleu3 | bleu4 |
| ------------- | ------------- | ------------- | ------------- | ----------- |
| Greedy search  | 0.26455 | 0.16700  | 0.106902 | 0.058529 |

`no Beam search due to timeouts` 


## Setup and running:

  #### Data preprocessing: `EDA_Medical_Report.ipynb`
    - Data loading 
    - Data visualisation
  #### Encoder decoder model: `baseline.ipynb`
    - Data sampling and split into `test.pkl` and `train.pkl`
    - Model definition
    - Training
    - Evaluation
  #### Attention model: `attention_model.ipynb`
    - Model definition
    - Training
    - Evaluation

## Citations

- Ben Abacha, Asma. 2017. “NLM at ImageCLEF 2017 Caption Task.”

- Chempolil, Ashish Thomas. 2021. “Medical Image Captioning on Chest X-Rays.” Medical Image Captioning on Chest X-Rays.

- “GloVe: Global Vectors for Word Representation.” 2014. 1.

- Hochreiter, Sepp, and Juurgen Schmidhuber. 1997. “LONG SHORT-TERM MEMORY.”

- Karpathy, Andrej, and Li Fei-Fei. 2015. “Deep Visual-Semantic Alignments for Generating Image Descriptions.”

- Kingma, Diederik P, and Jimmy Lei Ba. 2015. “ADAM: A METHOD FOR STOCHASTIC OPTIMIZATION.”

- Papineni, Kishore, and Wei-Jing Zhu. 2002. “BLEU: a Method for Automatic Evaluation of Machine Translation.” Proceedings of the 40th Annual Meeting of the Association for Computational Linguistics (ACL), Philadelphia, July 2002, pp. 311-318.

- Rajpurkar, Pranav. 2017. “CheXNet: Radiologist-Level Pneumonia Detection on Chest X-Rays with Deep Learning.”

- Reddy, Raj. 2001. “Spoken language processing: A guide to theory, algorithm, and system development.”

- Tang, Quan, and Yu Zhang. 2020. “Attention-guided Chained Context Aggregation for Semantic Segmentation.” 1.

- Vinyals, Oriol, and Alexander Toshev. 2015. “Show and Tell: A Neural Image Caption Generator.”