---
title: IDebugObject2::GetICorDebugValue |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugObject2::GetICorDebugValue
helpviewer_keywords:
- IDebugObject2::GetICorDebugValue method
ms.assetid: bcd4355d-3fbe-483f-bb23-a44348323c6a
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 313d3fdd2c56f4e38a9cb703f9aeb1a3aef1e73e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49199870"
---
# <a name="idebugobject2geticordebugvalue"></a>IDebugObject2::GetICorDebugValue
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

获取表示与此对象关联的值的托管的代码对象。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetICorDebugValue(  
   IUnknown** ppUnk  
);  
```  
  
```csharp  
int GetICorDebugValue(  
   out object ppUnk  
);  
```  
  
#### <a name="parameters"></a>参数  
 `ppUnk`  
 [out]`IUnknown`接口，表示此别名。 此接口可以查询有关`ICorDebugValue`接口。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回 S_OK;否则，返回错误代码。  
  
## <a name="remarks"></a>备注  
 `ICorDebugValue`对象是一个公共语言运行时接口，表示的值。  
  
## <a name="see-also"></a>请参阅  
 [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)
