---
title: Code de notification NM_RDBLCLK (arborescence) (commctrl. h)
description: Avertit le parent d’un contrôle Tree-View que l’utilisateur a double-cliqué sur le bouton droit de la souris dans le contrôle. Cette notification est envoyée sous la forme d’un \_ message WM Notify.
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- Contrôles Windows de code de notification NM_RDBLCLK (arborescence)
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5b4f1dbaf1031c995028028cc0b44e544f5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105283"
---
# <a name="nm_rdblclk-tree-view-notification-code"></a>\_Code de notification RDBLCLK nm (arborescence)

Avertit le parent d’un contrôle Tree-View que l’utilisateur a double-cliqué sur le bouton droit de la souris dans le contrôle. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RDBLCLK

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



 

 





