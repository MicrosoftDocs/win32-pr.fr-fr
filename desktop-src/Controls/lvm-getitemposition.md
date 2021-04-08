---
title: Message LVM_GETITEMPOSITION (commctrl. h)
description: Récupère la position d’un élément de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemPosition.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- LVM_GETITEMPOSITION les contrôles de message Windows
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
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844101"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

