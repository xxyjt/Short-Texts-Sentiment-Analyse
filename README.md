### Short-Texts-Sentiment-Analyse
Emotional Analyse of Chinese Short Texts with Several Method

### 基于中文短文本的情感分析对比实验
情感分析的方法大概分为四类：情感词典法、机器学习方法、深度学习方法、基于预训练模型微调
接下来对以上几种方法的建模思路和模型优缺点进行介绍：

情感词典法：利用人为标注或者评级过的情感字典，通过将文本进行分词，利用分词后的数据匹配字典中的值，然后直接加权或者利用词性进行加权即得到整句话的情感得分，最后根据专家经验或者数据分布，选取正、负的临界值作为模型的阈值。

机器学习方法：机器学习方法的思想是，将情感分析任务当作一个分类任务，通过将短文本转化为固定维度的向量，利用当前基于不同思想的分类器对其进行训练，通过对比测试集结果来观察不同的机器学习分类器之间的差异。

深度学习方法：深度学习是近年来较为热门的领域，其基于神经网络，利用网络的自适应学习率不断调节损失函数的值，大大减少了人工调参的复杂度，并且由于目前计算机算力水平的大幅度提升，利用GPU加速运算使得在短时间内即可得到较好的效果。比较主流的深度学习做情感分析的方法是利用长短期记忆模型来捕获句子之前的前后联系，得到相比于机器学习更好的效果，而本文从多层感知机、BP神经网络、卷积神经网络、长短期记忆神经网络以及自注意力机制模型来进行对比实验从而探索各种深度学习模型在情感分析领域的优缺点。

基于预训练模型微调：finetune是当前各类NLP任务的首选，由于2018年BERT模型刷新了各项NLP任务的最优，使得预训练模型成为目前的研究热点，最近基于自回归的XLNet又刷新了NLP任务的sota，可以看到未来的研究热点还是会集中在预训练模型。本文利用预训练好的BERT模型在情感分析领域做迁移训练，观察其效果，并对比最新的XLNet，研究两种预训练模型的优缺点。

情感词典法的优点：优点是建模方法简单，运算速度快，灵活多变，针对不同场景有可调的参数结构和方式。
情感词典法的缺点：缺点是构建词典需要耗费大量人力物力，深入挖掘行业信息，迁移能力弱，即针对不同领域需要构建不同的行业情感词典，另外其模型的效果以及各类别的准确率、召回率均比较低，对于含有不同情感类别的句子分类效果很差。

机器学习的优点：优点是相比于情感词典法，机器学习利用词向量进行建模，挖掘其特征，利用特征建模，效果较好，模型较小，并且场景容易做不同行业之间的迁移。
机器学习的缺点：模型所需调节的参数较多，并且很多参数需要人工不断尝试，（类似kaggle，得到top1的调参基本都是玄学问题）。

深度学习方法的优点：相比于机器学习，其模型效果更好，泛化能力更好，场景迁移能力较强，泛化能力好
深度学习方法的缺点：对于数据数量以及质量的要求较高，如果数据量太少，容易引发过拟合，数据质量不好模型很难收敛，并且其相比于其他方法，比较耗时。

BERT的优缺点：
XLNet的优缺点：

# 具体既然少

1.逻辑回归
2.随机梯度下降
3.朴素贝叶斯
4.支持向量机
5.随机森林
6.XGBoost


