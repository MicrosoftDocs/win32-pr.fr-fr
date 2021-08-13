---
title: Message LVM_GETORIGIN (commctrl. h)
description: Récupère l’origine de la vue actuelle pour un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetOrigin.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- LVM_GETORIGIN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a274e81c276d70eb1ab6c7f214b62ae5c346a59dda026bb13c5ab6b3ce80f68d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411356"
---
# <a name="lvm_getorigin-message"></a>\_Message GETORIGIN LVM

Récupère l’origine de la vue actuelle pour un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) qui reçoit l’origine de la vue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** si la vue actuelle est une liste ou un affichage des rapports.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

