# Attention is all you need

## 1.摘要

>&#160; &#160; &#160; &#160;The dominant sequence transduction models are based on complex recurrent or convolutional neural networks that include
> an encoder and a decoder. The best performing models also connect the encoder and decoder through an attention mechanism. 
> We propose a new simple network architecture, the Transformer, based solely on attention mechanisms, dispensing with recurrence
> and convolutions entirely. Experiments on two machine translation tasks show these models to be superior in quality while being 
> more parallelizable and requiring significantly less time to train. Our model achieves 28.4 BLEU on the WMT 2014 Englishto-German 
> translation task, improving over the existing best results, including ensembles, by over 2 BLEU. On the WMT 2014 English-to-French 
> translation task, our model establishes a new single-model state-of-the-art BLEU score of 41.0 
> after training for 3.5 days on eight GPUs, a small fraction of the training costs of the best models from the literature.


>&#160; &#160; &#160; &#160;主要的序列转导（如英文句子序列-中文句子序列）模型基于复杂的递归或卷积神经网络，该神经网络包括编码器和解码器。性能最好的模型还通过注意力机制将编码器和解码器连接起来。
(我们提出了一种新的简单的网络体系结构Transformer，**它完全基于注意力机制，完全不需要Recurrence&#40;循环）和卷积**。在两个机器翻译任务上的实验表明，这些模型在质量上更优越，)
(同时具有更高的并行化能力，所需的训练时间显著减少。我们的模型在WMT 2014英译德翻译任务中获得了28.4%的BLEU成绩，比现有的最好成绩&#40;包括语料库&#41;提高了2%以上。)
在WMT 2014英法翻译任务上，我们的模型在8个GPU上进行了3.5天的培训后，建立了新的单一模型最先进的BLEU得分41.0，这只是文献中最好的模型的培训成本的一小部分。

## 多头注意力机制 multi-head attention

Transformer作为之后语言大模型LLM，多模态大模型MLLM，图像大模型VLM的基础，重点是先要理解其内部结构。
多头注意力是很多人没搞懂的点，在不清楚其内部如何运转的情况下就去继续学习大模型，就会在后续遇到很多问题。




