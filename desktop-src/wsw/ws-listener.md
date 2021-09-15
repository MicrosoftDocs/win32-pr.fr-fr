---
title: WS_LISTENER (WebServices. h)
description: Type opaque utilisé pour référencer un écouteur.
ms.assetid: 2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa
keywords:
- WS_LISTENER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 803bde20292a55d1c3f2b7ca216ba3631e9116a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521993"
---
# <a name="ws_listener"></a>\_écouteur WS

Type opaque utilisé pour référencer un [écouteur](listener.md).


```C++
typedef struct _WS_LISTENER WS_LISTENER;
```



## <a name="remarks"></a>Notes

Cet objet est thread-safe. Pour plus d’informations, consultez [sécurité des threads](thread-safety.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>WebServices. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Port d'écoute](listener.md)
</dt> <dt>

[Cohérence de thread](thread-safety.md)
</dt> </dl>

 

 





