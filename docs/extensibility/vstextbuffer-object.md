---
title: VSTextBuffer 对象 |Microsoft Docs
description: VSTextBuffer 对象表示 Unicode 文本流，该流通常与文件相关联。 本文列出了 VSTextBuffer 的接口。
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- VSTextBuffer
helpviewer_keywords:
- VSTextBuffer object, reference
- views [Visual Studio SDK], VSTextBuffer object
ms.assetid: c5f94b45-7249-4e1f-a53d-1d2a1c61e0ef
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e5c2afa08e9c480342bff95d417dfb9174250b83
ms.sourcegitcommit: dd96a95d87a039525aac86abe689c30e2073ae87
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/04/2021
ms.locfileid: "97863953"
---
# <a name="vstextbuffer-object"></a>VSTextBuffer 对象
文本缓冲区对象表示 Unicode 文本流，该流通常与文件相关联。 <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer>对象可用于核心编辑器上下文之外，如向导中所示。

 下表显示了的接口 `VSTextBuffer` 。

|方法|说明|
|------------|-----------------|
|[IOleCommandTarget](/windows/desktop/api/docobj/nn-docobj-iolecommandtarget)|标准 OLE 接口。 用于在缓冲区中进行撤消/重做处理。|
|[IPersistFile](/windows/desktop/api/objidl/nn-objidl-ipersistfile)|标准 OLE 接口。|
|[IPersistStream](/windows/desktop/api/objidl/nn-objidl-ipersiststream)|标准 OLE 接口。|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsCompoundAction>|启用 (的 "组合" 操作，即在单个 "撤消/重做" 单元中分组) 的操作。|
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData>|启用由文本缓冲区管理的文档数据的持久性。|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer>|提供基本服务;由许多客户端使用。|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextFind>|用于搜索缓冲区。|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines>|使用二维坐标提供读写功能。 继承自 `IVsTextBuffer`。|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextStream>|使用一维坐标提供读写功能。 继承自 `IVsTextBuffer`。|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextScanner>|为缓冲区中的文本提供快速、面向流的顺序访问。|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsUserData>|提供对属性的泛型集合的访问。 最重要的属性是缓冲区的名称或名字对象。 可以通过创建 GUID 并将其用作密钥，在缓冲区中存储你自己的随机数据。|
|<xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer>|支持事件的连接点。|

## <a name="remarks"></a>备注
 `VSTextBuffer`通常通过对的调用找到 `QueryInterface` `IVsTextBuffer` 。 有关详细信息，请参阅 [文本缓冲区](/previous-versions/visualstudio/visual-studio-2015/extensibility/accessing-the-text-buffer-by-using-the-legacy-api?preserve-view=true&view=vs-2015)。

## <a name="see-also"></a>另请参阅
- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer>
- <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView>
- [编辑图形](https://www.microsoft.com/download/details.aspx?id=55984)