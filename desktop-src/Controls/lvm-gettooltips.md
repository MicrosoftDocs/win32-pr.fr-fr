---
title: Message LVM_GETTOOLTIPS (commctrl. h)
description: Récupère le contrôle ToolTip que le contrôle List-View utilise pour afficher des info-bulles. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetToolTips.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- LVM_GETTOOLTIPS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999796"
---
# <a name="lvm_gettooltips-message"></a>\_Message GETTOOLTIPS LVM

Récupère le contrôle ToolTip que le contrôle List-View utilise pour afficher des info-bulles. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le handle du contrôle ToolTip.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTOOLTIPS LVM**](lvm-settooltips.md)
</dt> </dl>

 

 





