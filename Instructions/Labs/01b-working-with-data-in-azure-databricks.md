---
lab:
    title: '在 Azure Databricks 中使用数据'
    module: '模块 1 - Azure Databricks 简介'
---

# 在 Azure Databricks 中使用数据

你将了解如何使用 DBFS 加载数据以及如何使用 Spark 数据帧处理数据。
Databricks 文件系统 (DBFS) 是一个挂载到 Databricks 工作区的分布式文件系统，可以在 Databricks 群集上使用。
数据帧是分布式数据集合，可处理大量数据。

## 先决条件

开始本实验室之前，请完成“**Azure Databricks 入门**”实验室，设置 Azure Databricks 环境并导入所需的数据和笔记本。

## 在 Azure Databricks 中使用数据

在此练习中，你将了解如何在 Azure Databricks 环境中加载和处理数据。

1. 在 Web 浏览器中，打开 Azure Databricks 工作区。

1. 如果群集未运行，请在“**计算**”页面上，选择群集并按“**&#9654;  启动**”按钮启动该群集

1. 在 Azure Databricks 工作区的左侧命令栏中，选择“**工作区**”。然后，选择“**用户**”和 **&#9751; your_user_name**。然后，在名为“**01 - Azure Databricks 简介**”的文件夹中，打开“**在 Azure Databricks 中使用数据**”笔记本。

1. 将笔记本附加到群集。然后阅读笔记本中的笔记，依次运行每个代码单元。

## 清理

如果当前完成了使用 Azure Databricks，请在 Azure Databricks 工作区的“**计算**”页面上，选择你的群集，然后选择“**&#9632; 终止**”以将其关闭。否则，让它继续运行以便你在下一个练习中使用。
