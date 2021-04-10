---
title: LVN_DELETEITEM le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’un élément est sur le point d’être supprimé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- Contrôles Windows de code de notification LVN_DELETEITEM
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106672"
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

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

N’ajoutez pas, ne supprimez pas ou ne réorganisez pas les éléments en mode liste lors du traitement de ce code de notification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





