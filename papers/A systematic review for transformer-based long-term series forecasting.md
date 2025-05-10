# A systematic review for transformer-based long-term series forecasting

## Abstract

The emergence of deep learning has yielded noteworthy advancements in time series forecasting (TSF). Transformer architectures have witnessed broad utilization and adoption in TSF tasks. Transformers have proven to be the most successful solution to extract the semantic correlations among the elements within a long sequence. Various variants have enabled Transformer architecture to effectively handle long-term time series forecasting (LTSF) tasks. In this article, we first present a comprehensive overview of Transformer architectures and their subsequent enhancements developed to address various LTSF tasks. Then, we summarize the publicly available LTSF datasets and relevant evaluation metrics. Furthermore, we provide valuable insights into the best practices and techniques for effectively training Transformers in the context of time-series analysis. Lastly, we propose potential research directions in this rapidly evolving field.

深度学习的出现为时间序列预测（TSF）带来了显著的进展。Transformer架构在TSF任务中得到了广泛的应用和采纳。Transformers已被证明是提取长序列中元素间语义相关性的最成功解决方案。各种变体使得Transformer架构能够有效地处理长期时间序列预测（LTSF）任务。在本文中，我们首先全面概述了Transformer架构及其为解决各种LTSF任务而开发的后续改进。然后，我们总结了公开可用的LTSF数据集和相关的评估指标。此外，我们提供了关于在时间序列分析背景下有效训练Transformers的最佳实践和技术的宝贵见解。最后，我们提出了在这个快速发展的领域中的潜在研究方向。

## 1 Introduction

The time series is usually a set of random variables observed and recorded sequentially over time. Key research directions for time-series data are classification [1, 2], anomaly detection [3–5], event prediction [6–8], and time series forecasting [9–11]. Time series forecasting (TSF) predicts the future trend changes of time series from a large amount of data in various fields. With the development of data collection technology, the task gradually evolves into using more historical data to predict the longer-term future, which is long-term time series forecasting (LTSF) [12, 13]. Precise LTSF can offer support to decision makers to better plan for the future by forecasting outcomes further in advance, including meteorology prediction [14], noise cancellation [15], financial long-term strategic guidance [16], power load forecasting [17, 18], and traffic road condition prediction [19].

时间序列通常是一组随时间顺序观察和记录的随机变量。时间序列数据的关键研究方向包括分类[1, 2]、异常检测[3-5]、事件预测[6-8]和时间序列预测[9-11]。时间序列预测（TSF）是从各个领域大量的数据中预测时间序列未来趋势的变化。随着数据收集技术的发展，该任务逐渐演变为使用更多的历史数据来预测更长期的未来，这就是长期时间序列预测（LTSF）[12, 13]。精确的LTSF可以为决策者提供支持，通过提前更长时间预测结果来更好地规划未来，应用范围包括气象预测[14]、噪声消除[15]、金融长期战略指导[16]、电力负荷预测[17, 18]以及交通路况预测[19]。

