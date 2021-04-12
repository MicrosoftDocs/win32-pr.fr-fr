---
title: Message LVM_SETTOOLTIPS (commctrl. h)
description: Définit le contrôle ToolTip que le contrôle List-View utilisera pour afficher des info-bulles. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetToolTips.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- LVM_SETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464879"
---
# <a name="lvm_settooltips-message"></a>\_Message SETTOOLTIPS LVM

Définit le contrôle ToolTip que le contrôle List-View utilisera pour afficher des info-bulles. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Handle du contrôle ToolTip à définir.</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du contrôle ToolTip précédent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETTOOLTIPS LVM**](lvm-gettooltips.md)
</dt> </dl>

 

 





