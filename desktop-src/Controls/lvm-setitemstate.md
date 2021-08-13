---
title: Message LVM_SETITEMSTATE (commctrl. h)
description: Modifie l’état d’un élément dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetItemState.
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- LVM_SETITEMSTATE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b7375ad7edb32459fe6029081ec0a872d3673c90003e34ca21cd795d3a79ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217414"
---
# <a name="lvm_setitemstate-message"></a>\_Message SETITEMSTATE LVM

Modifie l’état d’un élément dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément de vue de liste. Si ce paramètre a la valeur-1, le changement d’État est appliqué à tous les éléments.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Le membre **stateMask** spécifie les bits d’État à modifier, et le membre d' **État** contient les nouvelles valeurs pour ces bits. Les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si vous envoyez ce message de manière explicite, il retourne **true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

La valeur d’état d’un élément comprend un jeu d’indicateurs binaires qui indiquent l’état de l’élément. La valeur d’État peut également inclure des index de liste d’images qui indiquent l’image d’état de l’élément et l’image de superposition.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





