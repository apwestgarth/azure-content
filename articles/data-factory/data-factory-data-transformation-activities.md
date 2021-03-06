<properties 
	pageTitle="Azure Data Factory - Data Transformation Activities" 
	description="Learn how you can use the Azure Data Factory service to transform and analyze data." 
	services="data-factory" 
	documentationCenter="" 
	authors="spelluru" 
	manager="jhubbard" 
	editor="monicar"/>

<tags 
	ms.service="data-factory" 
	ms.workload="data-services" 
	ms.tgt_pltfrm="na" 
	ms.devlang="na" 
	ms.topic="article" 
	ms.date="07/26/2015" 
	ms.author="spelluru"/>

# Transform and analyze using Azure Data Factory
Transformation activities in Azure Data Factory transform and process your raw data into predictions and insights. The transformation activity executes in a computing environment such as Azure HDInsight cluster or an Azure Batch. Azure Data Factory supports the following transformation activities that can be added to [pipelines](data-factory-create-pipelines.md) either individually or chained with another activity.

Transformation activity |  Compute environment 
----------------------- | --------------------
[Hive](data-factory-hive-activity.md) | HDInsight [Hadoop] 
[Pig](data-factory-pig-activity.md) | HDInsight [Hadoop]  
[MapReduce](data-factory-map-reduce.md) | HDInsight [Hadoop]  
[Hadoop Streaming](https://msdn.microsoft.com/library/mt185698.aspx) | HDInsight [Hadoop]
[Machine Learning Batch Scoring](data-factory-create-predictive-pipelines.md) | Azure VM 
[Stored Procedure](https://msdn.microsoft.com/library/mt185717.aspx) | Azure SQL | 
[DotNet](data-factory-use-custom-activities.md) | HDInsight [Hadoop] or Azure Batch    

For HDInsight, We support the following two types of HDInsight linked service configurations:

1. [On-Demand](https://msdn.microsoft.com/library/mt185733.aspx):  In this case, the computing environment is fully managed by Data Factory. It is automatically created by the Data Factory service before a job is submitted to process data and removed when the job is completed. Users can configure and control granular settings of the on-demand compute environment for job execution, cluster management, and bootstrapping actions. 
2. [Bring Your Own](https://msdn.microsoft.com/library/mt185697.aspx): In this case, you can register your own computing environment (for example HDInsight cluster) as a linked service in Data Factory. The computing environment is managed by you and the Data Factory service uses it to execute the activities. 

See [Azure SQL Linked Service](https://msdn.microsoft.com/library/mt185705.aspx), [Azure Batch Linked Service](https://msdn.microsoft.com/library/mt185713.aspx), and [Azure Machine Learning Linked Service](https://msdn.microsoft.com/library/mt185726.aspx) for details about using Azure SQL, Azure Batch, and Azure Machine Learning compute environments. 

 
 


