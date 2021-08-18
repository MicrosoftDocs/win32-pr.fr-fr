---
title: Code de notification NM_CLICK (arborescence) (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle Tree-View sur lequel l’utilisateur a cliqué avec le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 39b5716d-cae7-4dc4-b257-0118f4f432c6
keywords:
- NM_CLICK (arborescence) code de notification Windows les contrôles
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
ms.openlocfilehash: d9d942504afd13359f38fa62c4f6a283367288873f89922311242516b9063990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018887"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





