---
title: TVN_ENDLABELEDIT le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View de la fin de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- TVN_ENDLABELEDIT les contrôles de Windows de code de notification
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
ms.openlocfilehash: 38be7b9fde4b96f3510cd59683ee9df471cc4d77342fe375d9b1818b8ae7da46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408199"
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

## <a name="remarks"></a>Remarques

Si le membre **pszText** a la valeur **null**, la valeur de retour est ignorée.

Si vous avez spécifié la \_ valeur LPSTR TEXTCALLBACK pour cet élément et que le membre **pszText** n’est pas **null**, votre \_ Gestionnaire TVN ENDLABELEDIT doit copier le texte de **pszText** dans votre stockage local.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ ENDLABELEDITW** (Unicode) et **TVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





