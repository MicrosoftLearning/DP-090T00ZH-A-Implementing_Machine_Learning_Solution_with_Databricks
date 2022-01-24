---
lab:
    title: 'Azure Databricks 入门'
    module: '模块 1 - Azure Databricks 简介'
---

# Azure Databricks 入门

Azure Databricks 是基于 Spark 的快速、简单、协作型分析服务。该服务可用于加速大数据分析、人工智能、高性能 Data Lake、交互式数据科学、机器学习和协作。
你将了解 Azure Databricks 环境及其相关的主要主题：工作区、群集、笔记本。

首先，你需要使用交互式群集访问 Azure Databricks 工作区。如果没有工作区和/或所需的群集，请按照下面的说明操作。否则，可以跳至下方的“**上传数据**”部分。

## 创建 Azure Databricks 资源

若要使用 Azure Databricks，首先需要在 Azure 订阅中部署 Azure Databricks 工作区，然后创建将在其中运行笔记本和代码的群集。然后，可以上传数据和笔记本，以在工作区中进行试验。

### 部署 Azure Databricks 工作区

1. 在 [Azure 门户](https://portal.azure.com)中，创建新的 **Azure Databricks** 资源，并指定以下设置：
   - **订阅**： *选择要在其中部署工作区的 Azure 订阅。*
   - **资源组**： *创建新的资源组。*
   - **工作区名称**： *为工作区提供名称。*
   - **区域**： *选择你附近的位置进行部署。有关 Azure Databricks 支持的区域列表，请参阅[按区域提供的 Azure 服务](https://azure.microsoft.com/regions/services/)。*
   - **定价层**：标准

1. 等待工作区创建完毕。创建工作区需要几分钟时间。在创建工作区过程中，门户会在右侧显示“正在提交 Azure Databricks 的部署”磁贴。可能需要在仪表板上向右滚动才能看到该磁贴。另外，还会在屏幕顶部附近显示进度条。你可以查看任意一个区域以了解进度。

### 创建群集

1. 创建 Azure Databricks 工作区资源后，在门户中转到该资源，然后选择“**启动工作区**”，在新选项卡中打开 Databricks 工作区，并在出现提示时登录。

1. 在 Databricks 工作区的左侧菜单中，选择“**计算**”，然后选择“**+ 创建群集**”，添加新群集并采用以下配置：
   - **名称**： *输入唯一名称。*
   - **群集模式**：单节点
   - **池**：无
   - **Databricks Runtime 版本**： *选择最新版运行时的 **ML** 版本。确保选中该版本：*
      - ***不**使用 GPU*
      - *包括 Scala > **2.11***
      - *包括 Spark > **3.0***
   - **终止时间**：非活动时间达到 120 分钟时
   - **节点类型**： Standard_DS3_v2

1. 等待群集创建完毕，这可能需要几分钟的时间。群集将自动启动，最后群集名称旁边旋转的“*暂停*”指示符将变为绿色实心圆圈，以指示“*正在运行*”状态。

### 上传数据

1. 将 `https://raw.githubusercontent.com/MicrosoftLearning/dp-090-databricks-ml/master/data/nyc-taxi.csv` 下载到计算机，并在任意文件夹中将其另存为 **nyc-taxi.csv**。

1. 在 Databricks 工作区的“**数据**”页上，选择“**创建表**”选项。

1. 在“**文件**”区域中，选择“**浏览**”，然后浏览下载的 **nyc-taxi.csv** 文件。

1. 将文件上传到工作区后，选择“**使用 UI 创建表**”。然后，选择群集并选择“**预览表**”。

1. 指定以下表属性：

    - **表名称**：nyc_taxi
    - **在数据库中创建**：默认
    - **文件类型**： CSV
    - **列分隔符**：, *（逗号）*
    - **第一行作为标题**： *已选中*
    - **推理模式**： *已选中*
    - **多行**： *取消选中*

1. 为每一列设置适当的数据类型：找到 **passengerCount** 列。在下拉菜单中，将列设置为“**INT**”。

    - passengerCount： **INT**
    - tripDistance：**DOUBLE**
    - hour_of_day： **INT**
    - day_of_week：**INT**
    - month_num：**INT**
    - isPaidTimeOff：**BOOLEAN**
    - snowDepth：**DOUBLE**
    - precipTime：**DOUBLE**
    - precipDepth：**DOUBLE**
    - temperature：**DOUBLE**
    - totalAmount：**DOUBLE**

1. 单击“**创建表**”。

1. 创建表后，请在工作区中查看。

### 导入 Databricks 笔记本

1. 在 Azure Databricks 工作区的左侧命令栏中，选择“**工作区**”。然后，选择“**用户**”和 **&#9751; your_user_name**。

1. 在显示的边栏选项卡中，选择名称旁边的向下指向 V 形符号 (**v**)，然后选择“**导入**”。

1. 在“**导入笔记本**”对话框中，从以下 URL 导入笔记本存档，注意系统会创建一个与存档同名的文件夹，其中包含一个或多个笔记本：
   - `https://github.com/MicrosoftLearning/dp-090-databricks-ml/raw/master/01%20-%20Introduction%20to%20Azure%20Databricks.dbc`

1. 重复上一步，导入以下笔记本存档，注意在导入每一个存档时，系统会为其创建一个文件夹。

   - `https://github.com/MicrosoftLearning/dp-090-databricks-ml/raw/master/02%20-%20Training%20and%20Evaluating%20Machine%20Learning%20Models.dbc`
   - `https://github.com/MicrosoftLearning/dp-090-databricks-ml/raw/master/03%20-%20Managing%20Experiments%20and%20Models.dbc`
   - `https://github.com/MicrosoftLearning/dp-090-databricks-ml/raw/master/04%20-%20Integrating%20Azure%20Databricks%20and%20Azure%20Machine%20Learning.dbc`

## 探索 Azure Databricks

在此练习中，你将了解 Azure Databricks 环境。

1. 在工作区中的“**01 - Azure Databricks 简介**”文件夹中，打开“**Azure Databricks 入门**”笔记本。

1. 在左上角的下拉菜单中，选择群集，将笔记本附加到该群集。 *（或者，在未附加的笔记本中运行第一个单元时，系统会提示附加群集）。*

1. 阅读笔记本中的笔记，依次运行每个代码单元。

## 清理

如果当前完成了使用 Azure Databricks，请在 Azure Databricks 工作区的“**计算**”页面上，选择你的群集，然后选择“**&#9632; 终止**”以将其关闭。否则，让它继续运行以便你在下一个练习中使用。
