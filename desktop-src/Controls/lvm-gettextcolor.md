---
title: Message LVM_GETTEXTCOLOR (commctrl. h)
description: Récupère la couleur de texte d’un contrôle List View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetTextColor.
ms.assetid: 51685e61-dd0a-4c21-8c66-31cf72c2b3e4
keywords:
- LVM_GETTEXTCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4ea7d295d87b8db5d0fa43403ccd01a8b41790447fd7ed6b7bae5d08150c934
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079043"
---
# <a name="lvm_gettextcolor-message"></a>\_Message GETTEXTCOLOR LVM

Récupère la couleur de texte d’un contrôle List View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la couleur du texte.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





