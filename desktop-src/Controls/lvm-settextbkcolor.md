---
title: Message LVM_SETTEXTBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan du texte dans un contrôle de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetTextBkColor.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- LVM_SETTEXTBKCOLOR les contrôles de Windows de message
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
ms.openlocfilehash: 3d9acdc193609f39fb81aa88263724a507695f15dcb8ba0c789df5c2a4f4d128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656229"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





