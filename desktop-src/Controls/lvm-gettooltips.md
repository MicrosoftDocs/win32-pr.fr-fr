---
title: Message LVM_GETTOOLTIPS (commctrl. h)
description: Récupère le contrôle ToolTip que le contrôle List-View utilise pour afficher des info-bulles. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetToolTips.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- LVM_GETTOOLTIPS les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466503"
---
# <a name="lvm_gettooltips-message"></a>\_Message GETTOOLTIPS LVM

Récupère le contrôle ToolTip que le contrôle List-View utilise pour afficher des info-bulles. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du contrôle ToolTip.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTOOLTIPS LVM**](lvm-settooltips.md)
</dt> </dl>

 

 





