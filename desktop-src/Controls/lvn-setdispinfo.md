---
title: LVN_SETDISPINFO le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’il doit mettre à jour les informations qu’il gère pour un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- Contrôles Windows de code de notification LVN_SETDISPINFO
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942480"
---
# <a name="lvn_setdispinfo-notification-code"></a>\_Code de notification LVN SETDISPINFO

Avertit la fenêtre parente d’un contrôle List-View qu’il doit mettre à jour les informations qu’il gère pour un élément. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) qui spécifie les informations relatives à l’élément modifié. Le membre d' **élément** de cette structure est une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) qui contient des informations sur l’élément qui a été modifié. Le membre **pszText** de l' **élément** contient une valeur valide, que l’indicateur de \_ texte LVIF soit défini ou non dans le membre de **masque** de cette structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le récepteur de notification convertit *lParam* pour récupérer la structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Le paramètre *wParam* contient le code du message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVN \_ SETDISPINFOW** (Unicode) et **LVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[LVN \_ GETDISPINFO](lvn-getdispinfo.md)
</dt> </dl>

 

 





