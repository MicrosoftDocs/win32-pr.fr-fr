---
title: Code de notification NM_DBLCLK (arborescence) (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle Tree-View que l’utilisateur a double-cliqué sur le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2ed3b3ad-a252-496a-bfcf-0cec5678f192
keywords:
- Contrôles Windows de code de notification NM_DBLCLK (arborescence)
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f89671e1a26962eacf255d4c98ea0baa1578de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032348"
---
# <a name="nm_dblclk-tree-view-notification-code"></a>\_Code de notification DBLCLK nm (arborescence)

Avertit la fenêtre parente d’un contrôle Tree-View que l’utilisateur a double-cliqué sur le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_DBLCLK
        
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



 

 





