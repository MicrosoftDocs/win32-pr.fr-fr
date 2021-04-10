---
title: LVN_BEGINLABELEDIT le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View à propos du début de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- Contrôles Windows de code de notification LVN_BEGINLABELEDIT
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f77550b474534cee096b610a0805bce547d9b429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941710"
---
# <a name="lvn_beginlabeledit-notification-code"></a>\_Code de notification LVN BEGINLABELEDIT

Avertit une fenêtre parente d’un contrôle List-View à propos du début de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Le membre d' **élément** de cette structure est une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dont le membre **iItem** identifie l’élément en cours de modification. Notez que les sous-éléments ne peuvent pas être modifiés ; le membre **iSubItem** est toujours défini sur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour permettre à l’utilisateur de modifier l’étiquette, retournez **false**.

Pour empêcher l’utilisateur de modifier l’étiquette, retournez la **valeur true**.

## <a name="remarks"></a>Notes

Lorsque la modification d’étiquette commence, un contrôle d’édition est créé, positionné et initialisé. Avant qu’il ne soit affiché, le contrôle List-View envoie sa fenêtre parente à un \_ Code de notification LVN BEGINLABELEDIT.

Pour personnaliser la modification des étiquettes, implémentez un gestionnaire pour LVN \_ BEGINLABELEDIT et envoyez-lui un message [**\_ GETEDITCONTROL LVM**](lvm-geteditcontrol.md) vers le contrôle List-View. Si une étiquette est en cours de modification, la valeur de retour est un handle pour le contrôle d’édition. Utilisez ce handle pour personnaliser le contrôle d’édition en envoyant les messages **em \_ xxx** habituels.

Lorsque l’utilisateur annule ou termine la modification, la fenêtre parente reçoit un code de notification [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVN \_ BEGINLABELEDITW** (Unicode) et **LVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





