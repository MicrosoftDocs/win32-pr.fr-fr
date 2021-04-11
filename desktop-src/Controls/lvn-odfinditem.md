---
title: Message LVN_ODFINDITEM (commctrl. h)
description: Envoyé par un contrôle List-View virtuel lorsqu’il a besoin du propriétaire pour rechercher un élément de rappel particulier.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- LVN_ODFINDITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104812"
---
# <a name="lvn_odfinditem-message"></a>\_Message LVN ODFINDITEM

Envoyé par un contrôle [List-View virtuel](list-view-controls-overview.md) lorsqu’il a besoin du propriétaire pour rechercher un élément de rappel particulier. Par exemple, le contrôle enverra ce code de notification lorsqu’il reçoit une entrée au clavier du raccourci ou lorsqu’il reçoit un message [**\_ FINDITEM LVM**](lvm-finditem.md) . Le \_ Code de notification LVN ODFINDITEM est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) qui contient des informations à utiliser pour la recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de l’élément trouvé, ou-1 si aucun élément n’est trouvé.

## <a name="remarks"></a>Notes

Les informations de recherche sont envoyées sous la forme d’une structure [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , qui est membre de la structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVN \_ ODFINDITEMW** (Unicode) et **LVN \_ ODFINDITEMA** (ANSI)<br/>             |



 

 





