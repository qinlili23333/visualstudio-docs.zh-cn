---
title: PROFILE_CURRENTID | Microsoft Docs
description: 了解如何使用 PROFILE_CURRENTID 使函数在当前线程或进程上运行，而不是在具体指示的线程或进程上运行。
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- PROFILE_CURRENTID
ms.assetid: 55ccf665-a05e-48c3-adf7-7714c0a9aaef
author: mikejo5000
ms.author: mikejo
manager: jillfra
monikerRange: vs-2017
ms.workload:
- multiple
ms.openlocfilehash: 5171753ff8ea6722cf1d97e155352e3899fb5562
ms.sourcegitcommit: 18729d7c99c999865cc2defb17d3d956eb3fe35c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/23/2021
ms.locfileid: "98719482"
---
# <a name="profile_currentid"></a>PROFILE_CURRENTID
在调用 NameProfile、StartProfile、StopProfile、SuspendProfile 和 ResumeProfile 函数时，PROFILE_CURRENTID 会返回线程 ID 或进程 ID 的伪标记。 使用此属性可使函数在当前线程或进程上运行，而不是在具体指示的线程或进程上运行。

## <a name="example-1"></a>示例 1
 PROFILE_CURRENTID 在 VSPerf.h 中定义为：

```cpp
static const unsigned int PROFILE_CURRENTID = (unsigned int)-1;
```

## <a name="example-2"></a>示例 2
 下面的示例演示 PROFILE_CURRENTID。 该示例将 PROFILE_CURRENTID 用作 [StartProfile](../profiling/startprofile.md) 函数调用中标识当前线程的参数。

```cpp
void ExerciseProfileCurrentID()
{
    // Declare ProfileOperationResult enumeration
    // to hold return value of a call to StartProfile.
    PROFILE_COMMAND_STATUS profileResult;

    // Variables used to print output.
    HRESULT hResult;
    TCHAR tchBuffer[256];

    profileResult = StartProfile(
        PROFILE_GLOBALLEVEL,
        PROFILE_CURRENTID);

    // Format and print result.
    LPCTSTR pszFormat = TEXT("%s %d.\0");
    TCHAR* pszTxt = TEXT("StartProfile returned");
    hResult = StringCchPrintf(tchBuffer, 256, pszFormat,
        pszTxt, profileResult);

#ifdef DEBUG
    OutputDebugString(tchBuffer);
#endif
}
```

## <a name="see-also"></a>请参阅
- [Visual Studio 探查器 API 参考（本机）](../profiling/visual-studio-profiler-api-reference-native.md)
- [NameProfile](../profiling/nameprofile.md)
- [ResumeProfile](../profiling/resumeprofile.md)
- [StartProfile](../profiling/startprofile.md)
- [StopProfile](../profiling/stopprofile.md)
- [SuspendProfile](../profiling/suspendprofile.md)
