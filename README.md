# Nihao: Relative Fine-Grained Chinese Word Segmentation

#### Important Updates

For CCL-2021 Shared Task: 2021-04-01

[CCL2021-SharedTask-Link](http://www.cips-cl.org/static/CCL2021/cclEval/taskEvaluation/index.html)

Official Website: 2021-05-01

[Evaluation-Link](http://114.116.55.241/sharedTask-unsupervisedCWS)



#### Description of the Corpus


Word is the fundamental unit in natural language processing (NLP) and is easy to obtain because of the natural delimiters between words. However, the situation is totally different when dealing with the Chinese language. Chinese sentences consist of continuous characters without the natural delimiters. Therefore, Chinese word segmentation (CWS) has become the first step (pre-processing) of Chinese NLP tasks, which splits Chinese sentences into independent words and significantly affects the quality of downstream Chinese NLP tasks. 

Different with the popular CWS benchmark datasets, we extract texts from downstream NLP tasks associated with Chinese. The corpus is open-domain and is closer to the real-world scenario. And we propose a relative fine-grained criterion for adapting downstream NLP tasks. In particular, the consistency of corpus is an inevitable problem on every segmentation benchmark due to high linguistic complexities of languages. Thus, we propose the **Consistency Checking**  to improve the quality of **'Nihao'** .



#### Evaluation on the Corpus

For demonstrating the quality of **'Nihao'** corpus, we adopt two outstanding proposals. In particular, we utilize the work by [(Huang et al., 2020)](#reference) for validating the  **Consistency** of the corpus (Note: we adopt the K cross-validation to train the model by the test data itself). And we utilize the work by [(Sun and Deng, 2018)](#reference) as a baseline of unsupervised training. 

The supervised baseline:

| K Cross-Validation (K=5)    | P      | R      | F      |
| --------------------------- | ------ | ------ | ------ |
| train-1,2,3,4 \|\|\| test-5 | 0.9855 | 0.9852 | 0.9854 |
| train-1,2,3,5 \|\|\| test-4 | 0.9854 | 0.9875 | 0.9865 |
| train-1,2,4,5 \|\|\| test-3 | 0.9847 | 0.9863 | 0.9855 |
| train-1,3,4,5 \|\|\| test-2 | 0.9850 | 0.9856 | 0.9853 |
| train-2,3,4,5 \|\|\| test-1 | 0.9845 | 0.9865 | 0.9855 |

The unsupervised baseline:

| Method                              | P      | R      | F      |
| ----------------------------------- | ------ | ------ | ------ |
| [(Sun and Deng, 2018)](#reference) | 0.8064 | 0.7847 | 0.7954 |




#### Resources

We provide several external resources for a better understanding of **'Nihao'** and unsupervised segmentation methods.

1. [segmentation criterion with the dictionary of Chinese affix.](https://github.com/koukaiu/nihao/blob/main/res/nihao_segmentation_criterion.pdf) 
3. the dictionary of long words in common use, which is modified by [(Cai and Zhao, 2016)](#reference). [Link](https://github.com/koukaiu/nihao/blob/main/res/idiomsDUTNLP)

External resources ([Download Link](https://github.com/koukaiu/nihao/tree/main/res))



#### Groups and Contact Information

-DUTNLP Lab: the Natural Language Processing Lab at Dalian University of Technology

Leader: Degen Huang

Members: Kaiyu Huang, Wei Liu, Hao Yu



-Contact us. 

If you have questions, suggestions and bug reports, please email us (unsupervisedCWS@163.com).



#### Reference

1. Kaiyu Huang, Degen Huang, Zhuang Liu and Fengran Mo. 2020. [A Joint Multiple Criteria Model in Transfer Learning for Cross-domain Chinese Word Segmentation.](https://www.aclweb.org/anthology/2020.emnlp-main.318/) In Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP), pages 3841--3847, Online. Association for Computational Linguistics.
2. Zhiqing Sun, Zhi-Hong Deng. 2018. [Unsupervised Neural Word Segmentation for Chinese via Segmental Language Modeling.](https://www.aclweb.org/anthology/D18-1531/) In Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing, pages 4915--4920, Brussels, Belgium. Association for Computational Linguistics.
3. Deng Cai and Hai Zhao. 2016. [Neural Word Segmentation Learning for Chinese.](https://www.aclweb.org/anthology/P16-1039/) In Proceedings of the 54th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pages 409–420, Berlin, Germany. Association for Computational Linguistics.



------

Copyright © 2021 DUTNLP Lab. All rights reserved.

