---
title: LVN_ITEMCHANGED le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’un élément a été modifié. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- Contrôles Windows de code de notification LVN_ITEMCHANGED
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c856292e9b94590b50593a6c3c5f145497f47f28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509761"
---
# <a name="lvn_itemchanged-notification-code"></a>\_Code de notification LVN ITEMCHANGED

Avertit la fenêtre parente d’un contrôle List-View qu’un élément a été modifié. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) qui identifie l’élément et spécifie quels attributs ont changé. Si le membre **iItem** de la structure vers laquelle pointe *lParam* a la valeur-1, la modification a été appliquée à tous les éléments de la vue liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Si un contrôle d’affichage de liste a le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) et que l’utilisateur sélectionne une plage d’éléments en maintenant la touche Maj enfoncée et en cliquant sur la souris, les \_ codes de notification LVN ITEMCHANGED ne sont pas envoyés pour chaque élément sélectionné ou désélectionné. Au lieu de cela, vous recevrez un code de notification [LVN \_ ODSTATECHANGED](lvn-odstatechanged.md) unique, indiquant que l’état d’une plage d’éléments a changé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





