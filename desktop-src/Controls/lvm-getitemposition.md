---
title: Message LVM_GETITEMPOSITION (commctrl. h)
description: Récupère la position d’un élément de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemPosition.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- LVM_GETITEMPOSITION les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d4f4a55f88b6af9828420871de80117ae492bf53c8a62883e43f928c4f5c70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002619"
---
# <a name="lvm_getitemposition-message"></a>\_Message GETITEMPOSITION LVM

Récupère la position d’un élément de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément de vue de liste.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) qui reçoit la position de l’angle supérieur gauche de l’élément, dans les coordonnées de la vue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

