---
title: NM_OUTOFMEMORY le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le contrôle n’a pas pu terminer une opération, car la mémoire disponible est insuffisante. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- NM_OUTOFMEMORY les contrôles de Windows de code de notification
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
ms.openlocfilehash: c8a2efdd0048006b86d97964dc953d2dbd7c4ecb2687b3c0fb67a5effc63fea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958108"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





