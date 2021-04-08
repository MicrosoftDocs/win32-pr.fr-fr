---
title: LVN_HOTTRACK le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View lorsque l’utilisateur déplace la souris sur un élément. Ce code de notification est uniquement envoyé par les contrôles List-View qui ont \_ le \_ style LVS ex TRACKSELECT Extended List-View. Il est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- Contrôles Windows de code de notification LVN_HOTTRACK
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677b69fa21cdbe3680442304f6745cfb3a907de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844474"
---
# <a name="lvn_hottrack-notification-code"></a>\_Code de notification LVN HOTTRACK

Envoyé par un contrôle List-View lorsque l’utilisateur déplace la souris sur un élément. Ce code de notification est uniquement envoyé par les contrôles List-View qui ont le style [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) Extended List-View. Il est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) qui contient des informations sur ce code de notification. Les membres **iItem**, **iSubItem** et **ptAction** de cette structure contiennent des informations sur l’élément. L’application réceptrice peut modifier le membre **iItem** pour spécifier l’élément qui sera sélectionné. Si **iItem** a la valeur-1, aucun élément n’est sélectionné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro pour permettre à la vue de liste d’effectuer son traitement de sélection normal. Si l’application retourne une valeur différente de zéro, l’élément n’est pas sélectionné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





