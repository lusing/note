# Deep Learning for Time Series Forecasting: A Survey

## Abstract

Time series forecasting has become a very intensive field of research, which is even increasing in recent years. Deep neural networks have proved to be powerful and are achieving high accuracy in many application fields. For these reasons, they are one of the most widely used methods of machine learning to solve problems dealing with big data nowadays. In this work, the time series forecasting problem is initially formulated along with its mathematical fundamentals. Then, the most common deep learning architectures that are currently being successfully applied to predict time series are described, highlighting their advantages and limitations. Particular attention is given to feed forward networks, recurrent neural networks (including Elman, long-short term memory, gated recurrent units, and bidirectional networks), and convolutional neural networks. Practical aspects, such as the setting of values for hyperparameters and the choice of the most suitable frameworks, for the successful application of deep learning to time series are also provided and discussed. Several fruitful research fields in which the architectures analyzed have obtained a good performance are reviewed. As a result, research gaps have been identified in the literature for several domains of application, thus expecting to inspire new and better forms of knowledge.

时间序列预测已成为一个非常热门的研究领域，并且近年来其热度还在不断上升。深度神经网络已被证明功能强大，并且在许多应用领域中都能达到很高的精度。基于这些原因，如今深度神经网络是解决大数据相关问题时最广泛使用的机器学习方法之一。
在这项研究工作中，首先阐述了时间序列预测问题及其数学基础。然后，描述了目前成功应用于时间序列预测的最常见的深度学习架构，并着重介绍了它们的优点和局限性。特别关注了前馈网络、循环神经网络（包括埃尔曼网络、长短期记忆网络、门控循环单元以及双向网络）和卷积神经网络。文中还给出并讨论了深度学习成功应用于时间序列预测的一些实际操作方面的内容，比如超参数值的设置以及最合适框架的选择。
此外，对若干个已分析的架构在其中取得良好性能的富有成果的研究领域进行了综述。由此，在文献中识别出了多个应用领域中存在的研究空白，期望以此激发新的、更优的知识形式。

## Introduction

The interest in processing huge amounts of data has experienced a rapid increase during the past decade due to the massive deployment of smart sensors1 or the social media platforms,2 which generate data on a continuous basis.3 However, this situation poses new challenges, such as storing these data in disks or making available the required computational resources.

在过去十年里，由于智能传感器的大规模部署，以及社交媒体平台的广泛应用，人们对处理海量数据的关注度迅速上升。这些智能传感器和社交媒体平台会持续不断地产生数据。然而，这种情况带来了新的挑战，比如如何将这些数据存储在磁盘中，以及如何提供所需的计算资源。

Big data analytics emerges, in this context, as an essential process focused on efficiently collecting, organizing, and analyzing big data with the aim of discovering patterns and extracting valuable information. In most organizations, this helps to identify new opportunities and making smarter moves, which leads to more efficient operations and higher profits.

在这种背景下，大数据分析应运而生，它是一个至关重要的过程，专注于高效地收集、整理和分析大数据，目的是发现数据中的模式并提取有价值的信息。在大多数组织中，这有助于识别新的机会并做出更明智的决策，进而实现更高效的运营并获得更高的利润。

From all the learning paradigms that are currently
being used in big data, deep learning highlights
because of its outstanding performance as the
scale of data increases.6 Most of the layer computations
in deep learning can be done in parallel by, for
instance, powerful graphic processing units (GPUs).
That way, scalable distributed models are easier to
be built and they provide better accuracy at a much
higher speed. Higher depth allows for more complex
non-linear functions but, in turn, with higher computational
costs.

