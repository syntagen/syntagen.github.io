---
layout: schedule
order: 4
permalink: /challenge
title: Challenge
# redirect_from: /index.html
desc_title: SyntaGen Competition
# description: <strong>The Good, the Bad and the Ugly</strong> - Modern AI development requires using and sharing of models and data safely. Uncovering backdoor, a foe and a friend at the front door.
social: true
---
* TBD

<!-- The primary objective of this competition is to drive innovation in the creation
of high-quality synthetic datasets, leveraging only the pretrained [Stable Diffusion (version 2.1)](https://huggingface.co/spaces/stabilityai/stable-diffusion) 
and the 20 class names from [PASCAL VOC 2012](http://host.robots.ox.ac.uk/pascal/VOC/voc2012/) for semantic segmentation. The evaluation of synthetic dataset quality involves training a [DeepLabv3](https://arxiv.org/abs/1706.05587) model on the synthetic dataset and subsequently assessing its performance on a private test set on the task of semantic segmentation. Submissions are ranked based on the **mIoU** metric. This competition framework mirrors the practical
application of synthetic datasets, particularly in scenarios where they replace real datasets.

### Requirements
Teams are required to upload their synthetic datasets to **Google Drive** for public
access. The dataset should include a maximum of **10K** pairs of synthesized images and semantic
segmentations, each image being **512x512** in size. We will supply a Google Colab codebase for
exemplifying some random training images and their annotations, DeepLabv3 training and evaluation,
using a **Resnet-50** backbone, and showing qualitative results. Training and evaluation time for
DeepLabv3 is capped at **100K iterations** with a **batch size of 8**. The codebase should remain
unchanged except for the Google Drive file ID provided by each team. For text prompts, participants
can leverage various methods, including LLMs like ChatGPT4. For text-to-image generation, only
**Stable Diffusion (v2.1)** is permissible. However, participants can freely modify Stable Diffusion without retraining as they wish.

### Submission and evaluation
The submission comprises two phases with two separate deadlines,
outlined as follows:

1.  **Random seed + DeepLabv3 + Dataset**. By the first deadline in this phase, each team
must use their method to generate their synthetic dataset and train a DeepLabv3 on it. Each
team must submit: 1. the random seed used in their model for dataset generation, 2. the
generated dataset, and 3. the checksum of the trained DeepLabv3. The checksum code
will be provided as part of the Colab codebase. Modifications to the model, the trained
DeepLabv3, or the generated dataset are prohibited after this deadline.

2.  **Code + Score**. After the first deadline, our private test set will be released to each team.
Each team must evaluate their trained DeepLabv3 on the test set and submit their Colab
code and mIoU score by the final deadline.

We will use our provided Google Colab setup to replicate the submitted results, encompassing both
training and evaluation. We will also verify the generated images and annotations to ensure they are reproducible with the submitted random seed, fully synthetic, and not derived from inversion of real images or the PASCAL VOC dataset. Moreover, awarded teams are obliged to share their **dataset synthesis code on GitHub**, confirming adherence to Stable Diffusion version 2.1 as the sole text-to-image generator. Submissions are ranked by their mIoUs, and any non-compliant entries that violate any rules will be excluded from consideration.

### Prizes and presentation: 

We will award the top 2 teams with cash prizes and invite them to write a report and present their work at the workshop.

### Ethical considerations for the datasets
Since the evaluated dataset is the validation set of PASCAL
VOC 2012, it shares the same ethical considerations with PASCAL VOC 2012. Besides, the generated synthetic training set has new considers including:

<!-- * **Data Bias and Fairness**: The creation of synthetic datasets through Stable Diffusion -->
<!-- can introduce unintended biases, potentially deviating from real-world data characteristics.
Ethical vigilance is essential to identify and rectify any biases, ensuring that the synthetic datasets remain representative, unbiased, and fair

* **Privacy and Consent**: Although synthetic datasets do not involve real individuals’ data,
traces of underlying characteristics might inadvertently capture sensitive information. Upholding ethical principles necessitates the thorough anonymization or removal of such data
traces to protect privacy and respect consent standards. --> 