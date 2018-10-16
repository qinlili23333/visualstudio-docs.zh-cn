---
title: 'Idiasession:: Get_loadaddress |Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::get_loadAddress method
ms.assetid: 5162ae1a-38e3-4571-8995-4ed9be1dec3e
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fec8f9ed59d46b6865bbf96d0b341eb4bcc434bc
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49306171"
---
# <a name="idiasessiongetloadaddress"></a>IDiaSession::get_loadAddress
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

检索对应于此符号存储区中的符号的可执行文件的加载地址。  
  
## <a name="syntax"></a>语法  
  
```cpp#  
HRESULT get_loadAddress (   
   ULONGLONG* pRetVal  
);  
```  
  
#### <a name="parameters"></a>参数  
 `pRetVal`  
 [out]返回一个虚拟地址 (VA) 加载的.exe 文件或.dll 文件的位置。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回错误代码。  
  
## <a name="remarks"></a>备注  
 返回的加载地址始终为零，除非专门设置了使用[idiasession:: Put_loadaddress](../../debugger/debug-interface-access/idiasession-put-loadaddress.md)方法。  
  
## <a name="see-also"></a>请参阅  
 [IDiaSession](../../debugger/debug-interface-access/idiasession.md)   
 [IDiaSession::put_loadAddress](../../debugger/debug-interface-access/idiasession-put-loadaddress.md)


