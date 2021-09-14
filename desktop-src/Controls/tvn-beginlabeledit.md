---
title: TVN_BEGINLABELEDIT le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View du début de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- TVN_BEGINLABELEDIT les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34eccdeda553d0792a2862e3ca81a0889539d5ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115534"
---
# <a name="tvn_beginlabeledit-notification-code"></a>\_Code de notification TVN BEGINLABELEDIT

Avertit une fenêtre parente d’un contrôle Tree-View du début de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . Le membre de l' **élément** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient des informations valides sur l’élément en cours de modification dans les membres **hitem**, **State**, **lParam** et **pszText** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** pour annuler la modification de l’étiquette.

## <a name="remarks"></a>Notes

Lorsque la modification d’étiquette commence, un contrôle d’édition est créé mais pas positionné ou affiché. Avant qu’il ne soit affiché, le contrôle Tree-View envoie sa fenêtre parente un \_ Code de notification TVN BEGINLABELEDIT.

Pour personnaliser la modification des étiquettes, implémentez un gestionnaire pour TVN \_ BEGINLABELEDIT et envoyez un message [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) au contrôle Tree-View. Si une étiquette est en cours de modification, la valeur de retour est un handle pour le contrôle d’édition. Utilisez ce handle pour personnaliser le contrôle d’édition en envoyant les messages EM xxx habituels \_ .

Lorsque l’utilisateur annule ou termine la modification, la fenêtre parente reçoit un code de notification [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ BEGINLABELEDITW** (Unicode) et **TVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





