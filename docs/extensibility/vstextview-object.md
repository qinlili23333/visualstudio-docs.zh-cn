---
title: VSTextView 对象 |Microsoft Docs
description: VSTextView 对象是允许用户查看和编辑文本缓冲区的 Unicode 文本的窗口。
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- VSTextView
helpviewer_keywords:
- VSTextView object, reference
- views [Visual Studio SDK], reference
ms.assetid: 78272ddc-9718-4c65-a94e-a44a2e8d54f4
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9d7309e05c3763794deb344a978dd188dbfddd79
ms.sourcegitcommit: dd96a95d87a039525aac86abe689c30e2073ae87
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/04/2021
ms.locfileid: "97863815"
---
# <a name="vstextview-object"></a>VSTextView 对象

文本视图是允许用户查看和编辑文本缓冲区的 Unicode 文本的窗口。 实质上，视图是大多数用户作为编辑器引用的内容。 由于视图是由不同文本层与缓冲区分隔 (自动换行、大纲显示文本等) ，因此不能保证视图是缓冲区中的文本的精确表示形式。 有关文本视图的详细信息，请参阅 [使用旧 API 访问 theText 视图](/previous-versions/visualstudio/visual-studio-2015/extensibility/accessing-thetext-view-by-using-the-legacy-api?preserve-view=true&view=vs-2015)。

下表显示了对象中的接口 <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView> 。

|接口|说明|
|---------------|-----------------|
|[IDropSource](/windows/desktop/api/oleidl/nn-oleidl-idropsource)|标准 OLE 接口。|
|<xref:Microsoft.VisualStudio.OLE.Interop.IDropTarget>|标准 OLE 接口。|
|<xref:Microsoft.VisualStudio.OLE.Interop.IObjectWithSite>|标准 OLE 接口。|
|<xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>|标准 OLE 接口。|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsCompoundAction>|启用复合操作 (即，) 中的单个撤消/重做单元分组的操作。|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView>|提供用于管理和访问视图的基本方法。 `IVsTextView` 不是线程安全的。|
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane>|创建和管理窗口窗格。|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsLayeredTextView>|与文本层交互。|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsThreadSafeTextView>|从不同的线程对视图执行操作。|

## <a name="see-also"></a>另请参阅

- [编辑图形](https://www.microsoft.com/download/details.aspx?id=55984)
- [VSTextBuffer 对象](../extensibility/vstextbuffer-object.md)