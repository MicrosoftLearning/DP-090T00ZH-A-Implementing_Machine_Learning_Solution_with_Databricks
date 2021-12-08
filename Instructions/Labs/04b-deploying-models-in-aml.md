---
lab:
    title: '在 Azure 机器学习中部署模型'
    module: '模块 4 - 集成 Azure Databricks 和 Azure 机器学习'
---

# 在 Azure 机器学习中部署模型

机器学习主要是关于训练模型，你可以使用这些模型为应用程序提供预测服务。在本练习中，你将了解如何在 Azure Databricks 中训练模型，以及如何在 Azure 机器学习中部署模型。

## 先决条件

开始本实验室之前，请完成“**Azure Databricks 入门**”和“**在 Azure 机器学习中运行试验**”实验室，设置 Azure Databricks 和 Azure 机器学习环境。

## 在 Azure 机器学习中部署模型

在此练习中，你将了解如何在 Azure Databricks 环境中加载和处理数据。

1. 在 Web 浏览器中，打开 Azure Databricks 工作区。

1. 如果群集未运行，请在“**计算**”页面上，选择群集并按“**&#9654;  启动**”按钮启动该群集

1. 在 Azure Databricks 工作区的左侧命令栏中，选择“**工作区**”。然后，选择“**用户**”和 **&#9751; your_user_name**。然后，在名为“**04 - 集成 Azure Databricks 和 Azure 机器学习**”的文件夹中，打开“**2.0 在 Azure 机器学习中部署模型**”笔记本。

1. 将笔记本附加到群集。然后阅读笔记本中的笔记，依次运行每个代码单元。

## 清理

如果当前完成了使用 Azure Databricks，请在 Azure Databricks 工作区的“**计算**”页面上，选择你的群集，然后选择“**&#9632; 终止**”以将其关闭。

如果已完成对 Azure Databricks 的探索，则可以删除 Azure 订阅中包含 Azure Databricks 和 Azure 机器学习资源的资源组。
