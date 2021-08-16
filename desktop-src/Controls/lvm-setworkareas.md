---
title: Message LVM_SETWORKAREAS (commctrl. h)
description: Définit les zones de travail dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetWorkAreas.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- LVM_SETWORKAREAS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1060377fd9aec9014d18d206444355b052f4aafb796403e3e47fa92a0a7aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830660"
---
# <a name="lvm_setworkareas-message"></a>\_Message SETWORKAREAS LVM

Définit les zones de travail dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre de structures dans le tableau à *LPRC*. Le nombre maximal de zones de travail autorisées est défini par la \_ valeur LV Max \_ WORKAREAS.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau de structures [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contiennent les nouvelles zones de travail du contrôle List-View. Les valeurs de ces structures sont exprimées en coordonnées clientes. Si ce paramètre a la **valeur null**, la zone de travail est définie sur la zone cliente du contrôle. *wParam* spécifie le nombre de structures dans ce tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de contrôles List-View](using-list-view-controls.md)
</dt> </dl>

 

