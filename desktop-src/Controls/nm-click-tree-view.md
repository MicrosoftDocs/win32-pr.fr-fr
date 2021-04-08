---
title: Code de notification NM_CLICK (arborescence) (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle Tree-View sur lequel l’utilisateur a cliqué avec le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 39b5716d-cae7-4dc4-b257-0118f4f432c6
keywords:
- Contrôles Windows de code de notification NM_CLICK (arborescence)
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45809a683d06871398e79419ec08729b1edcd2c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743988"
---
# <a name="nm_click-tree-view-notification-code"></a>\_$ $ $, Cliquez (arborescence) Code de notification

Notifie la fenêtre parente d’un contrôle Tree-View sur lequel l’utilisateur a cliqué avec le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro pour empêcher le traitement par défaut, ou zéro pour autoriser le traitement par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





