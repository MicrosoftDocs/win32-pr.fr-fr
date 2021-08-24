---
title: WS_LISTENER (WebServices. h)
description: Type opaque utilisé pour référencer un écouteur.
ms.assetid: 2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa
keywords:
- WS_LISTENER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31fa7435ecea9770c2441a1c8c3d65c2d2346707c1c4e16da2f985e203d4ea3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083033"
---
# <a name="ws_listener"></a>\_écouteur WS

Type opaque utilisé pour référencer un [écouteur](listener.md).


```C++
typedef struct _WS_LISTENER WS_LISTENER;
```



## <a name="remarks"></a>Remarques

Cet objet est thread-safe. Pour plus d’informations, consultez [sécurité des threads](thread-safety.md).

## <a name="requirements"></a>Configuration requise



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

 

 





