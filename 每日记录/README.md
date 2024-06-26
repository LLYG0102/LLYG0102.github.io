# 每日记录
这个界面是用来记录每天的学习内容，以及遇见的问题，帮助进行工作记录。
## 2024.4.3
- 做了Transformer精读整理，QKV机制、缩放原因、多头注意力机制写了笔记。
- 链接在这里：[Transformer基础模型](/大模型LM/文献精读/Transformer.md)
- 还有几个问题待解决：tokenize方式、layernorm、位置编码（如何起效）、如何训练、如何推理
## 2024.3.21
- 增加了大模型笔记，整理网站结构
- 搜集顶会资源，为广泛阅读进行准备
- 读了CLIP，重点在其解决了面对固定任务需要给定分类器的问题。这是通过prompt engineering（输入输出都作为句子，而不是给定的类别标签），
让模型获得一定的理解语义的能力，使用对比学习，让模型只需要学习“图像-文本”的pair的配对。而拥有如此强大泛化能力的前提其实是巨大的数据支撑和大模型。
- 昨天读了MM1这个论文，一下引出了这个领域一大片的经典论文，transformer VIT CLiP DALL-E、MoCo等等，还有很多概念，对比学习、MoE。。坑实在是大。
## 2023.6.19
- 认真阅读了DTNN，这个课题组的大牛是Klaus-Robert Muller
## 2023.6.16-6.18
- 主要是休息，出了神经网络的期末考题
## 2023.6.12-6.15
- 休息，回了一趟家
## 2023.5.30-6.11
- 集合做导师的优青答辩ppt，加班了比较多，期间未更新
## 2023.5.29
- 完成了毕业答辩，过程比较顺利，老师评价：“讲得蛮清楚的，虽然我不太懂这个”
- 完成了PPT制作
## 2023.5.28
- 做了答辩准备
- 接到一个制作ppt的任务
## 2023.5.26
- 今天把DeepMD的精读做了，链接在[**这里**](../分子动力学机器学习/文献精读/DeepMD.md)，越看越觉得方法很妙。但依旧有几个问题：
> 里面的径向分布函数是什么意思？
> 损失函数最后一项什么意思，有什么用？
> 它适用于什么场景？然后有什么缺陷？
## 2023.5.25
- 今天做了答辩ppt，基本以图为主，明天可以选择看看文献或者写一下答辩的稿子。

## 2023.5.24
- 根据SchNet找到了他们课题组的代表作，K.-R. Müller，K. T. Schütt是经常出现的作者，应该是课题组的导师，他们是berlin技术大学的教授。同时找到的GDML也是早于DeepMD等方法提出的，论文篇幅不长，可以找时间好好看看。
- 今天当助教上台给同学们讲了一个小模型，感觉还不错，讲话需要多锻炼一下。助教还剩下周一一节课就结束了，1800到手。
- 在课间拿着结构化学书慢慢看，但是越看越困，看不进去，所以觉得知识还是搭配着文献和技术代码搭配学习，螺旋上升更好
- 明天争取一天做出PPT，今天有点摆。
## 2023.5.23
- 今天仔细阅读了SchNet，作为后续许多文章会拿来进行对比的baseline，它在当时所提出的概念还是比较新的，简单地做了一个精读，损失函数以及实验还没有写到，明天补上，连接在[**这里**](../分子动力学机器学习/文献精读/SchNet.md)。
>说实话这一篇文章我是带着很高的期待度去看的，然而越看越觉得失望，作者其实把很多简单的东西改了一个新名字，像atom-wise之类的，激活函数就写激活不就行了吗，用的什么函数在之后提一嘴就可以了，看到最后有一种以为是金子买回来发现是金包银的感觉。**还有以为会用上带有位置信息的相对位置坐标（在deepMD里就有用到），结果也只是拿了相对距离，我都觉得奇怪怎么这样也能拟合上力的方向呢？明明关于角度的信息都被压缩掉了。后续还需要好好再看看**
- 下午吃饭打算去换电，结果排队太长小哥直接送了我充电券（蔚来服务还是行啊），24小时免费随意次数充电（最多150度）。本着还没有给车充过电的态度去尝试了一下，结果发现充电是真的麻烦，给车充电的时间自己是在坐牢，一个小时干什么都比较尴尬，还是换电香啊~:smile:
- 今天读文献速度不快，效率有点低，需要调整。
- 今天发现大多数分子动力学的文章都发在很好的期刊上或者顶会，而思路也都差不太多，**针对分子体系的各种对称不变性（旋转、反射、平移），用不同的数据处理表示技术让同构但显式不同的数据变成同一种输入；或者让网络意识到这是同一种，那么就可以极大减小训练数据，甚至能做数据增强。再多读几天可以好好总结一下。**
## 2023.5.22
- ~~六点二十起床去奉贤校区当助教十一点回校，坐了一来一回两趟梦境，累死~~
- 为知识库增加一个**每周任务+计划表的模块**；
- 增加了项目进展分页，把项目进展、每周计划、每日记录放在同一模块中；
- 增加了评论插件，所有的评论会进入github的issues中
- 完成了基于MindSpore平台的word2vec模型教案制作，word2vec通过**词袋模型和skip-gram模型实现**，能够不依赖人工标注的语料库，把单词映射到连续、低维、稠密的向量空间中，从而实现单词的嵌入表示，通过这个表示可以计算单词之间的相似度，用作语义分析。
- 上传了先前完成的分子动力学-机器学习文献分类[**总结表格**](../项目进展记录/MolecularD.md#文献收集总结)，这也是之后需要精读的文献，
## 2023.5.21
- 使用了npm工具创建了一个个人知识库项目，已经部署到了**github pages**上，可以直接通过[**这个链接**](https://llyg0102.github.io)访问。
> 个人知识库的构建参考了[**b站上的项目**](https://www.bilibili.com/video/BV1eu411m797/?spm_id_from=333.337.search-card.all.click)，使用了docsify，这是作者第一次接触前端的工具和语言，搭建一个个人知识库是一个很有成就感的东西（~~即使什么知识都还没放~~），未来作者会研究加入更多功能和内容。    

docsify的 [**官方文档**](https://docsify.js.org/#/zh-cn/)

除了需要补充的知识内容和文献内容，目前能想到未来的工作有：
- **每日总结的界面需要加密**
- 文献分类，之后每一篇文献学习后用一个**单独的md文件进行介绍**，把文献中使用的原理和方法**链接上知识库内知识，做到知识的交叉链接**。