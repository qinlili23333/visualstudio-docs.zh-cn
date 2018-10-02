---
title: 如何：序列化符号信息 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VS.ToolsOptionsPages.Performance.General
helpviewer_keywords:
- profiling tools, serializing symbol information
- performance tools, serializing symbol information
ms.assetid: 9e0da706-6325-4073-83d1-aeab3b7c137a
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 04bce9383142ee6916fa7ade50feda072019f530
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47480612"
---
# <a name="how-to-serialize-symbol-information"></a>如何：序列化符号信息
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[如何： 序列化符号信息](https://docs.microsoft.com/visualstudio/profiling/how-to-serialize-symbol-information)。  
  
可以序列化分析应用程序所需的符号。 符号序列化的作用是将符号添加到 .vsp 文件中。 通过向 .vsp 文件添加符号信息，其他人可以在没有原始符号访问权限的情况下分析性能报告。 如果未序列化符号，则需要有受检测的原始 .exe 和 .pdb 文件才能分析 .vsp 文件。  
  
### <a name="to-automatically-serialize-symbol-information"></a>自动序列化符号信息  
  
1.  在 **“工具”** 菜单上，单击 **“选项”**。  
  
     随即出现“选项”对话框。  
  
2.  单击“性能工具”。  
  
3.  在“常规设置”下，选择“自动序列化符号信息”。  
  
## <a name="see-also"></a>请参阅  
 [配置性能会话](../profiling/configuring-performance-sessions.md)   
 [如何：引用 Windows 符号信息](../profiling/how-to-reference-windows-symbol-information.md)   
 [如何：保存已分析的报告文件](http://msdn.microsoft.com/en-us/0340ddde-caf4-48ac-8af3-d15dcdade556)


