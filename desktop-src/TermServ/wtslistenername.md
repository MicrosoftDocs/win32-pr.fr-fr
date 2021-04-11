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
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384952"
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



 

 





