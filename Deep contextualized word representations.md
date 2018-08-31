# Deep contextualized word representations
这篇文章发表在2018年的NAACL上，outstanding paper award。
近年来，研究人员通过文本上下文信息分析获得更好的词向量。ELMo是其中的翘楚，在多个任务、多个数据集上都有显著的提升。所以，它是目前最好用的词向量，the-state-of-the-art的方法。

##ELMo的优势
ELMo能够学习到词汇用法的复杂性，比如语法、语义。
ELMo能够学习不同上下文情况下的词汇多义性。

##ELMo的模型简介
基于大量文本，ELMo模型是从深层的双向语言模型（deep bidirectional language model）中的内部状态(internal state)学习而来的，而这些词向量很容易加入到QA、文本对齐、文本分类等模型中，后面会展示一下ELMo词向量在各个任务上的表现。

##双向语言模型
![image](https://raw.githubusercontent.com/max-yue/images/master/201.png)
![image](https://raw.githubusercontent.com/max-yue/images/master/202.png)
![image](https://raw.githubusercontent.com/max-yue/images/master/203.png) 

##ELMo
![image](https://raw.githubusercontent.com/max-yue/images/master/204.png)
![image](https://raw.githubusercontent.com/max-yue/images/master/205.png)
![image](https://raw.githubusercontent.com/max-yue/images/master/206.png)

##ELMo的效果
Textual entailment: stanford natural language inference (SNLI)数据集上提升了1.4%。
Question answering: 在stanford question answering dataset (SQuAD)数据集上提升了4.2%，将ELMo加入到之前的state-of-the-art的ensemble模型中，提升了10%。
Semantic role labeling: 比之前的state-of-the-art模型提高了3.2%，将ELMo加入到之前的state-of-the-art的单模型中，提升了1.2%。
Coreference resolution: 比之前的state-of-the-art模型提高了3.2%，将ELMo加入到之前的state-of-the-art的ensemble模型中，提升了1.6%。
Named entity extraction: 在CoNLL 2003 NER task数据机上提高了2.06%
Sentiment analysis: 比之前的state-of-the-art模型提高了3.3%，将ELMo加入到之前的state-of-the-art模型中，提升了1%。
