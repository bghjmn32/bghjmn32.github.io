---
title: "PageRankReport (2021/06/07-2021/06/11)"
date: 2021-06-11T22:44:21+02:00
Description: "Implemented textrank-based text summarization algorithm"
Tags: ["textrank",
    "text summarization",
    "motor design"]
Categories: ["LCM",
    "thesis",]
DisableComments: false
---
Starting from June 7th, I spent three days reading and implementing a page rank based text summarization algorithm.
<!--more-->

## PageRank

TextRank algorithm is a graph-based ranking algorithm for text, by partitioning text into several constituent units (sentences), constructing a node-linked graph, using the similarity between sentences as the weights of edges, calculating the TextRank values of sentences through circular iterations, and finally extracting the sentences with high ranking to combine into a text summary.


## Algorithm

The first step is to integrate all articles into text data. Then we split the text into individual sentences and find vector representation (word vectors) for each sentence. After that, we calculate the similarity between the sentences vectors and store them in a matrix. In the next step, the similarity matrix is transformed into a graph structure with sentences as nodes and similarity scores as edges for sentence TextRank calculation. Finally, a certain number of the highest ranked sentences constitute the final summary.

## Evaluation

In our experiments, we found that the real problem lies in the evaluation. Traditional extractive abstracts rely on the use of BERT scores or similar mechanisms, which are evaluated by comparing the similarity of the abstract to the original text. This approach originally originated in the field of machine translation and has since been adopted for text summarization, however, in practice we have found that traditional evaluation methods are often used for general articles, which may involve entertainment and sports news, political commentary or fiction. In these articles, as mentioned earlier, there is a large amount of information redundancy and the same fact or knowledge is often mentioned repeatedly, so this evaluation method can be applied. However, in the specialized field of motor design, similarity can hardly be used to assess the quality of abstracts because of their low information redundancy and high logical coherence.

Based on these facts, we may have to resort to expert evaluation, which relies on the LCM motor engineers to give their subjective comments.

{{< figure src="https://i.imgur.com/3sUAaHn.png" alt="image" caption="main process of textrank algorithm" >}}

## Code

It can be found in [Colab](https://colab.research.google.com/drive/1WfXs6SeWdj64WwzxNCBJz7k1cV9zNZfV?usp=sharing) or my [Github](https://github.com/bghjmn32/LCM-projects)

## Overleaf

I write two new subsection about TextRank Text Summarization and added somethingf in LESK section

## 情绪

我也不知道他会不会认真看,反正写了就写了他也看不懂中文. 星期三雨那么大他觉得我骗他是我懒不想去,邮件里面还阴阳怪气的说我什么偷懒,没干到40小时,要我每天都老老实实的去坐着干活,就差说我是个废物骗子了,我真的是又气又笑.但是能怎么办呢,他是老师,我是学生,我英语也不好,吵不过他,只能忍着呗. 反正他也不在乎我怎么想,哎,真是一天比一天抑郁,那天忍不住了就跳楼了算了,活着是真的没意思,什么心理咨询这些都是扯淡,死亡才是惟一的解脱.