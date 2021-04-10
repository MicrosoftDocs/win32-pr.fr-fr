---
title: TVN_ENDLABELEDIT le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View de la fin de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- Contrôles Windows de code de notification TVN_ENDLABELEDIT
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103900"
---
# <a name="tvn_endlabeledit-notification-code"></a>\_Code de notification TVN ENDLABELEDIT

Avertit une fenêtre parente d’un contrôle Tree-View de la fin de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . Le membre d' **élément** de cette structure est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dont les membres **hitem**, **lParam** et **pszText** contiennent des informations valides sur l’élément qui a été modifié. Si la modification d’étiquette a été annulée, le membre **pszText** de la structure **TVITEM** est **null**; Sinon, **pszText** est l’adresse du texte modifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le membre **pszText** n’est pas **null**, retourne **true** pour définir l’étiquette de l’élément sur le texte modifié. Retourne **false** pour rejeter le texte modifié et revenir à l’étiquette d’origine.

## <a name="remarks"></a>Notes

Si le membre **pszText** a la valeur **null**, la valeur de retour est ignorée.

Si vous avez spécifié la \_ valeur LPSTR TEXTCALLBACK pour cet élément et que le membre **pszText** n’est pas **null**, votre \_ Gestionnaire TVN ENDLABELEDIT doit copier le texte de **pszText** dans votre stockage local.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ ENDLABELEDITW** (Unicode) et **TVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





