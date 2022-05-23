# casualReading
A casual record of the papers read


[Just Rank: Rethinking Evaluation with Word and Sentence Similarities](https://arxiv.org/pdf/2203.02679.pdf)
* 问题：目前文本表示的评估往往主要依靠相似度任务（词相似度，句相似度），但相似度任务存在1.人工标注相似度概念模糊2.与下游任务表现相关性差
* 方法：用正样本对embedding的距离（cos/l_2）在所有样本对距离中的rank来评估embedding质量，可用于词/句向量评估；收集词相似度/句相似度任务dataset构建dataset
* 结果：EvalRank结果与单纯相似度任务的结果相比，与下游任务的相关性更高
* 有趣的点：whitening方法对相似度任务效果很好，但是对下游任务没用-解释：whitening方法主要优化低相似度样本，但是下游任务中高相似度样本更重要；总的来说SimCSE还是非常强；如果把最新的一些方法用EvalRank评估一下它们还能超过SimCSE吗？

[Exploiting Language Model Prompts Using Similarity Measures:
A Case Study on the Word-in-Context Task](https://aclanthology.org/2022.acl-short.36.pdf)