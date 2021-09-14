---
title: LVN_DELETEITEM le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’un élément est sur le point d’être supprimé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- LVN_DELETEITEM les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009d39e78aa93d5c5230e9c1b06b84d2854a0d0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012318"
---
# <a name="lvn_deleteitem-notification-code"></a>\_Code de notification LVN DELETEITEM

Avertit la fenêtre parente d’un contrôle List-View qu’un élément est sur le point d’être supprimé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Le membre **iItem** identifie l’élément en cours de suppression. Si le contrôle n’a pas le style **LVS \_ OWNERDATA** , *lParam* correspond aux données définies par l’application associées à l’élément. Tous les autres membres de cette structure sont nuls.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

N’ajoutez pas, ne supprimez pas ou ne réorganisez pas les éléments en mode liste lors du traitement de ce code de notification.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





