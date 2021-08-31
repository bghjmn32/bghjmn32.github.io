---
title: "WinterComing"
date: 2021-08-31T20:02:08+02:00
Description: ""
Tags: [
    "Generative Text Summary",
    "text summarization",
    "motor design"
]
Categories: [
    "LCM",
    "thesis"
]
DisableComments: false
---
## This Summer

The work scheduled for July had to be postponed due to my family accident. The stated goal now is to use new models such as "PEGASUS" for text summarization.

## PEGASUS
What differentiates PEGASUS from previous SOTA models is the pre-training? The authors (Jingqing Zhang et. al.) hypothesizes that pre-training the model to output important sentences is suitable as it closely resembles what abstractive summarization needs to do. Using a metric called ROUGE1-F1, the authors were able to automate the selection of “important” sentences and perform pre-training of the model on a large corpus, i.e., 350 million web pages and 1.5 billion news articles.
With the pre-trained model, we can then perform fine-tuning of the model on the actual data which is of a much smaller quantity. In fact, evaluation results on various datasets showed that with just 1,000 training data, the model achieved comparable results to previous SOTA models. This has important practical implications as most of us will not have the resources to collect tens of thousands of document-summary pairs.

## Train materials
Although fortunately, PEGASUS can be a highly pre-trained model. However, we still need to consider how the training material should be collected if other models are to be used. The current idea is to explore this from some motor design books.

## Personal Life
After a whole summer of despair, I told myself you have to get your act together. Even though the worst series of things have happened to you over the past year or so, you still need to keep moving forward. Even though you can't do anything about the misfortune that happened 10,000 miles away, you can still live your own life.