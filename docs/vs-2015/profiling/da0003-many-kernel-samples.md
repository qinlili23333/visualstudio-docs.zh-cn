---
title: DA0003：大量内核样本 | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.rules.DA0003
- vs.performance.DA0003
- vs.performance.3
- vs.performance.rules.DAManyKernelSamples
ms.assetid: c1f46f77-eb95-42e5-b340-d86bc9de41b4
caps.latest.revision: 16
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ba55e787c3ee07bb94fde325832a2c6b09d8d984
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49200665"
---
# <a name="da0003-many-kernel-samples"></a>DA0003：大量内核样本
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

规则 Id |DA0003 |  
|类别 |分析工具使用情况 |  
|分析方法 |采样 |  
|消息 |在内核模式下具有很高比例的示例。 这可能表明 I/O 活动量很大或上下文切换的速率很高。 请考虑使用检测模式再次分析应用程序。 |  
|规则类型 |信息 |  
  
## <a name="cause"></a>原因  
 为应用程序收集的很大一部分调用堆栈样本在内核模式下执行。 请考虑使用其他分析方法分析应用程序。  
  
## <a name="rule-description"></a>规则说明  
 在 Windows 中，可以在内核模式或用户模式下执行代码。 （内核模式也称为特权模式。）只有低级系统代码（如设备驱动程序）才可在内核模式下运行。 用户模式应用程序可转换为内核模式，执行 I/O 操作、等待线程或进程同步基元，或执行系统调用。  
  
 如果要分析将大多数时间花费在以用户模式工作的应用程序，采样最为有效。 在内核模式下执行应用程序时，收集的样本数可以指示频繁的 I/O 操作，也可以指示发生的上下文切换。 无法使用采样方法对这两种操作进行调查。 如果进行过多的内核模式采样，采样数据可能不包含足够多的用户模式样本，因此无法实现统计数据上的显著性。  
  
## <a name="how-to-fix-violations"></a>如何解决冲突  
 请考虑使用以下选项之一再次分析应用程序：  
  
-   使用检测方法进行分析。  
  
-   提高采样率，尝试在用户模式下收集更多样本。


