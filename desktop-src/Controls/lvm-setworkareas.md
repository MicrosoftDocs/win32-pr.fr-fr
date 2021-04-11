---
title: Message LVM_SETWORKAREAS (commctrl. h)
description: Définit les zones de travail dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetWorkAreas.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- LVM_SETWORKAREAS les contrôles de message Windows
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
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942639"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de contrôles List-View](using-list-view-controls.md)
</dt> </dl>

 

