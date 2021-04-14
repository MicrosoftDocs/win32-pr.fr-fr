---
title: Message LVM_GETWORKAREAS (commctrl. h)
description: Récupère les zones de travail à partir d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetWorkAreas.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- LVM_GETWORKAREAS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466499"
---
# <a name="lvm_getworkareas-message"></a>\_Message GETWORKAREAS LVM

Récupère les zones de travail à partir d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre de structures [**Rect**](/previous-versions//dd162897(v=vs.85)) dans le tableau au niveau de *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau de structures [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoivent les zones de travail actuelles du contrôle List-View. Les valeurs de ces structures sont exprimées en coordonnées clientes. *wParam* spécifie le nombre de structures dans ce tableau.

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

 

