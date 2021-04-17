---
title: WS_HEAP (WebServices. h)
description: Type opaque utilisé pour référencer un objet de segment de mémoire.
ms.assetid: 1866f54f-26fc-4889-a88f-0d298a418bdc
keywords:
- WS_HEAP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d996d3a3905a7f247cfc84840e5aae4baa781f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465735"
---
# <a name="ws_heap"></a>\_tas WS

Type opaque utilisé pour référencer un objet de [segment de mémoire](heap.md) .


```C++
typedef struct _WS_HEAP WS_HEAP;
```



## <a name="remarks"></a>Notes

Cet objet n’est pas thread-safe. Pour plus d’informations, consultez [sécurité des threads](thread-safety.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>WebServices. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Système](heap.md)
</dt> <dt>

[Cohérence de thread](thread-safety.md)
</dt> </dl>

 

 





