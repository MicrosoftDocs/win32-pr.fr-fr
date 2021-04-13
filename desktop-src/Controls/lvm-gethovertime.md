---
title: Message LVM_GETHOVERTIME (commctrl. h)
description: Récupère la durée pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetHoverTime.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- LVM_GETHOVERTIME les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e243ece42f06ffe35eb31954d9ca0dd44957be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465879"
---
# <a name="lvm_gethovertime-message"></a>\_Message GETHOVERTIME LVM

Récupère la durée pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la durée, en millisecondes, pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné. Si la valeur de retour est (**DWORD**)-1, la durée de pointage est la durée de pointage par défaut.

## <a name="remarks"></a>Notes

La durée de survol affecte uniquement les contrôles d’affichage de liste qui ont le style de vue de liste étendu [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)ou [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





