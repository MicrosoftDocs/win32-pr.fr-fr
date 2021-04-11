---
title: NM_OUTOFMEMORY le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le contrôle n’a pas pu terminer une opération, car la mémoire disponible est insuffisante. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- Contrôles Windows de code de notification NM_OUTOFMEMORY
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1321f88360d168b13d16b36f984d9b797dc094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032420"
---
# <a name="nm_outofmemory-notification-code"></a>\_Code de notification OUTOFMEMORY nm

Avertit la fenêtre parente d’un contrôle que le contrôle n’a pas pu terminer une opération, car la mémoire disponible est insuffisante. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée par le contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





