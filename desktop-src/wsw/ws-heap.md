---
title: WS_HEAP (WebServices. h)
description: Type opaque utilisé pour référencer un objet de segment de mémoire.
ms.assetid: 1866f54f-26fc-4889-a88f-0d298a418bdc
keywords:
- WS_HEAP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ca6f8eb745fa53b035cdb79d068099e96d2e037c87c139f4b19c30f933ecac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926799"
---
# <a name="ws_heap"></a>\_tas WS

Type opaque utilisé pour référencer un objet de [segment de mémoire](heap.md) .


```C++
typedef struct _WS_HEAP WS_HEAP;
```



## <a name="remarks"></a>Remarques

Cet objet n’est pas thread-safe. Pour plus d’informations, consultez [sécurité des threads](thread-safety.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>WebServices. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Segment de mémoire (heap)](heap.md)
</dt> <dt>

[Cohérence de thread](thread-safety.md)
</dt> </dl>

 

 





