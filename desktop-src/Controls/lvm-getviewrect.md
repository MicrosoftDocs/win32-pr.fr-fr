---
title: Message LVM_GETVIEWRECT (commctrl. h)
description: Récupère le rectangle englobant de tous les éléments dans le contrôle List-View. La vue liste doit être en mode icône ou petite icône. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetViewRect.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- LVM_GETVIEWRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999798"
---
# <a name="lvm_getviewrect-message"></a>\_Message GETVIEWRECT LVM

Récupère le rectangle englobant de tous les éléments dans le contrôle List-View. La vue liste doit être en mode icône ou petite icône. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit le rectangle englobant. Toutes les coordonnées sont relatives à la zone visible du contrôle List-View.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

