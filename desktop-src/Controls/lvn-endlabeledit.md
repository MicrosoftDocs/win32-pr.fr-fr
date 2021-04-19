---
title: LVN_ENDLABELEDIT le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View de la fin de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- Contrôles Windows de code de notification LVN_ENDLABELEDIT
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527580"
---
# <a name="lvn_endlabeledit-notification-code"></a>\_Code de notification LVN ENDLABELEDIT

Avertit une fenêtre parente d’un contrôle List-View de la fin de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Le membre d' **élément** de cette structure est une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dont le membre **iItem** identifie l’élément en cours de modification. Le membre **pszText** de l' **élément** contient une valeur valide lorsque le \_ Code de notification ENDLABELEDIT LVN est envoyé, que l' \_ indicateur de texte LVIF soit défini ou non dans le membre **Mask** de la structure **LVITEM** . Si l’utilisateur annule la modification, le membre **pszText** de la structure **LVITEM** est **null**; Sinon, **pszText** est l’adresse du texte modifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le membre **pszText** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) est non **null**, retourne **true** pour définir l’étiquette de l’élément sur le texte modifié. Retourne **false** pour rejeter le texte modifié et revenir à l’étiquette d’origine.

Si le membre **pszText** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) est **null**, la valeur de retour est ignorée.

## <a name="remarks"></a>Notes

La valeur de retour de la procédure de boîte de dialogue est si le message a été géré. La deuxième valeur de retour doit être définie en appelant [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) avec **DWLP_MSGRESULT**.

Lorsque l’utilisateur commence à modifier une étiquette d’élément, la fenêtre parente du contrôle List-View reçoit un code de notification [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) . Lorsque l’utilisateur annule ou termine la modification, la fenêtre parente reçoit un \_ Code de notification LVN ENDLABELEDIT.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVN \_ ENDLABELEDITW** (Unicode) et **LVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





