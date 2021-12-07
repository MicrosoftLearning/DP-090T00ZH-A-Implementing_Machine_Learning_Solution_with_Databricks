---
lab:
    title: '在 Azure 机器学习中运行试验'
    module: '模块 4 - 集成 Azure Databricks 和 Azure 机器学习'
---

# 在 Azure 机器学习中运行试验

机器学习主要是关于训练模型，你可以使用这些模型为应用程序提供预测服务。在此练习中，你将了解如何在 Azure Databricks 的 Azure 机器学习中运行试验。

## 先决条件

开始本实验室之前，请完成“**Azure Databricks 入门**”实验室，设置 Azure Databricks 环境并导入所需的数据和笔记本。

## 在 Azure Databricks 群集上安装库

在群集中需要安装的某个 Python 库决定了要运行的笔记本。以下步骤将指导你添加这些依赖项。

- 在 Azure Databricks 工作区的“**群集**”部分，选择你的群集。请确保群集的状态是“**正在运行**”。
- 选择“**库**”链接，然后选择“**安装新库**”。
- 在“**库源**”中，选择“**PyPi**”，在“**包**”文本框中，键入 `azureml-sdk[databricks]` 并选择“**安装**”。
- 接下来，安装 `sklearn-pandas==2.1.0`
- 接下来，安装 `azureml-mlflow`

## 部署 Azure 机器学习工作区

1. 如果已在订阅中创建了 Azure 机器学习工作区，则可以跳至[练习：在 Azure 机器学习中运行试验](#Exercise-Running-experiments-in-Azure-Machine-Learning)部分。

1. 在 [Azure 门户](https://portal.azure.com/#home)中，创建新的资源：**机器学习**

1. 在显示的“创建机器学习工作区”对话框中，输入以下值：

   - **订阅**：选择自己的 Azure 订阅。
   - **资源组**：选择在其中部署了 Azure Databricks 工作区的资源组。
   - **工作区名称**：aml-ws
   - **区域**：选择最近的区域（Azure Databricks 工作区和 Azure 机器学习工作区可以位于不同位置）。

1. 查看并完成 Azure 机器学习工作区的创建。

## 在 Azure 机器学习中运行试验

在此练习中，你将了解如何在 Azure Databricks 环境中加载和处理数据。

1. 在 Web 浏览器中，打开 Azure Databricks 工作区。

1. 如果群集未运行，请在“**计算**”页面上，选择群集并按“**&#9654;  启动**”按钮启动该群集

1. 在 Azure Databricks 工作区的左侧命令栏中，选择“**工作区**”。然后，选择“**用户**”和 **&#9751; your_user_name**。然后，在名为“**04 - 集成 Azure Databricks 和 Azure 机器学习**”的文件夹中，打开“**1.0 在 Azure 机器学习中运行试验**”笔记本。

1. 将笔记本附加到群集。然后阅读笔记本中的笔记，依次运行每个代码单元。

## 清理

如果当前完成了使用 Azure Databricks，请在 Azure Databricks 工作区的“**计算**”页面上，选择你的群集，然后选择“**&#9632; 终止**”以将其关闭。否则，让它继续运行以便你在下一个练习中使用。
