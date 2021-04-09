---
title: Message LVM_GETVIEWRECT (commctrl. h)
description: Récupère le rectangle englobant de tous les éléments dans le contrôle List-View. La vue liste doit être en mode icône ou petite icône. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetViewRect.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- LVM_GETVIEWRECT les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033138"
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

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

