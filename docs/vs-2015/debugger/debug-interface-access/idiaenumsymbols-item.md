---
title: 'Idiaenumsymbols:: Item |Microsoft Docs'
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
- IDiaEnumSymbols::Item method
ms.assetid: 2bd1ec04-e677-4e32-8e32-33334f1eed77
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e2013bdb93f47dc5d64e48a44ca1b2eee0ddfd36
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49188262"
---
# <a name="idiaenumsymbolsitem"></a>IDiaEnumSymbols::Item
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

通过索引中检索一个符号。  
  
## <a name="syntax"></a>语法  
  
```cpp#  
HRESULT Item (   
   DWORD        index,  
   IDiaSymbol** symbol  
);  
```  
  
#### <a name="parameters"></a>参数  
 索引  
 [in]索引[IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)要检索对象。 索引是 0 到范围内`count`-1，其中`count`返回的[idiaenumsymbols:: Get_count](../../debugger/debug-interface-access/idiaenumsymbols-get-count.md)方法。  
  
 symbol  
 [out]返回[IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)对象，表示所需的符号。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回错误代码。  
  
## <a name="see-also"></a>请参阅  
 [IDiaEnumSymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)


