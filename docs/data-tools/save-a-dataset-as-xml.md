---
title: 将数据集另存为 XML
description: 将数据集另存为 XML。 通过调用数据集上的可用 XML 方法（如 GetXml 或 WriteXml）来访问数据集中的 XML 数据。
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: how-to
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- XML [Visual Basic], datasets
- data [Visual Studio], saving as XML
- datasets [Visual Basic], saving as XML
- saving data
ms.assetid: 68b8327c-ae05-49ff-b9ba-99183e70b52c
author: ghogen
ms.author: ghogen
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: e454aca47f9bf6425ef2dfd98747869c27523f2c
ms.sourcegitcommit: ed26b6e313b766c4d92764c303954e2385c6693e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "94434618"
---
# <a name="save-a-dataset-as-xml"></a>将数据集另存为 XML

通过调用数据集上的可用 XML 方法，访问数据集中的 XML 数据。 若要以 XML 格式保存数据，可以调用的 <xref:System.Data.DataSet.GetXml%2A> 方法或 <xref:System.Data.DataSet.WriteXml%2A> 方法 <xref:System.Data.DataSet> 。

调用 <xref:System.Data.DataSet.GetXml%2A> 方法将返回一个字符串，该字符串包含数据集中所有格式为 XML 的数据表中的数据。

调用 <xref:System.Data.DataSet.WriteXml%2A> 方法会将 XML 格式的数据发送到您指定的文件。

## <a name="to-save-the-data-in-a-dataset-as-xml-to-a-variable"></a>将数据集中的数据以 XML 形式保存到变量

- <xref:System.Data.DataSet.GetXml%2A> 方法会返回 <xref:System.String>。 声明类型的变量 <xref:System.String> ，并为其分配方法的结果 <xref:System.Data.DataSet.GetXml%2A> 。

     [!code-vb[VbRaddataSaving#12](../data-tools/codesnippet/VisualBasic/save-a-dataset-as-xml_1.vb)]
     [!code-csharp[VbRaddataSaving#12](../data-tools/codesnippet/CSharp/save-a-dataset-as-xml_1.cs)]

## <a name="to-save-the-data-in-a-dataset-as-xml-to-a-file"></a>将数据集中的数据以 XML 形式保存到文件中

- <xref:System.Data.DataSet.WriteXml%2A>方法具有多个重载。 声明一个变量，并为其分配一个有效路径，以便将该文件保存到。 下面的代码演示如何将数据保存到文件中：

     [!code-vb[VbRaddataSaving#13](../data-tools/codesnippet/VisualBasic/save-a-dataset-as-xml_2.vb)]
     [!code-csharp[VbRaddataSaving#13](../data-tools/codesnippet/CSharp/save-a-dataset-as-xml_2.cs)]

## <a name="see-also"></a>另请参阅

- [将数据保存回数据库](../data-tools/save-data-back-to-the-database.md)
