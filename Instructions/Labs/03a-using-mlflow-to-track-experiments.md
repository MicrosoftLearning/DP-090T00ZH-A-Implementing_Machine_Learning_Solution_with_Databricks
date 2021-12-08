---
lab:
    title: '使用 MLflow 跟踪试验'
    module: '模块 3 - 管理试验和模型'
---

# 使用 MLflow 跟踪试验

MLflow 是一个功能全面的模型跟踪和注册表系统。  在此练习中，你将使用 MLflow 来收集模型训练工件、指标和参数。  然后，你将能够通过 Azure Databricks UI 或以编程方式查看这些输出。首先，你需要使用交互式群集访问 Azure Databricks 工作区。如果没有工作区和/或所需的群集，请按照下面的说明操作。否则，可以跳至[上传 Databricks 笔记本存档](#Upload-the-Databricks-notebook-archive)部分。

## 先决条件

开始本实验室之前，请完成 [**Azure Databricks 入门**](Instructions/Labs/01a-introduction-to-azure-databricks.md)实验室，设置 Azure Databricks 环境并导入所需的数据和笔记本。若要使用 MLflow，需使用具有 **ML Databricks Runtime** 版本的计算群集，如设置实验室中所述。该运行时已包括 MLflow 的安装。

## 使用 MLflow 跟踪试验

在此练习中，你将了解如何在 Azure Databricks 环境中加载和处理数据。

1. 在 Web 浏览器中，打开 Azure Databricks 工作区。

1. 如果群集未运行，请在“**计算**”页面上，选择群集并按“**&#9654;  启动**”按钮启动该群集

1. 在 Azure Databricks 工作区的左侧命令栏中，选择“**工作区**”。然后，选择“**用户**”和 **&#9751; your_user_name**。然后，在名为“**03 - 管理试验和模型**”的文件夹中，打开“**01 - 使用 MLflow 跟踪试验**”笔记本。

1. 将笔记本附加到群集。然后阅读笔记本中的笔记，依次运行每个代码单元。

> **提示**：“**使用 Databricks UI 查看试验、运行和运行详细信息**”部分说明了要执行的操作，因为在笔记本外将涉及这些操作。  最简单的方法可能是在浏览器中打开另一个选项卡，然后一边查看笔记本中的说明，一边在该选项卡中执行这些操作。

## 清理

如果当前完成了使用 Azure Databricks，请在 Azure Databricks 工作区的“**计算**”页面上，选择你的群集，然后选择“**&#9632; 终止**”以将其关闭。否则，让它继续运行以便你在下一个练习中使用。
