---
title: WTSLISTENERNAME (WtsApi32. h)
description: Représente le nom d’un Services Bureau à distance écouteurs sur un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- WTSLISTENERNAMEW
- WTSLISTENERNAMEA
- WTSLISTENERNAME
- PWTSLISTENERNAME
- WTSLISTENERNAME
- PWTSLISTENERNAME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce0df52229670cd090dd900dda3c2284437297bedc25c69f12c980b9cc40d92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513839"
---
# <a name="wtslistenername"></a>WTSLISTENERNAME

Représente le nom d’un Services Bureau à distance écouteurs sur un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

**WTSLISTENERNAMEW**
</dt> <dd>

Nom Unicode de l’écouteur.

</dd> <dt>

**WTSLISTENERNAMEA**
</dt> <dd>

Pointeur vers le nom ANSI de l’écouteur.

</dd> <dt>

**WTSLISTENERNAME**
</dt> <dd>

Nom de l'écouteur.

</dd> <dt>

**PWTSLISTENERNAME**
</dt> <dd>

Pointeur vers le nom de l’écouteur.

</dd> <dt>

**WTSLISTENERNAME**
</dt> <dd>

Nom de l'écouteur.

</dd> <dt>

**PWTSLISTENERNAME**
</dt> <dd>

Pointeur vers le nom de l’écouteur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>WtsApi32. h</dt> </dl> |



 

 





