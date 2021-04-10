---
title: Message LVM_SETTEXTBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan du texte dans un contrôle de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetTextBkColor.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- LVM_SETTEXTBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032692"
---
# <a name="lvm_settextbkcolor-message"></a>\_Message SETTEXTBKCOLOR LVM

Définit la couleur d’arrière-plan du texte dans un contrôle de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Nouvelle couleur d’arrière-plan du texte. Il peut s’agir \_ de CLR None pour aucune couleur d’arrière-plan.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





