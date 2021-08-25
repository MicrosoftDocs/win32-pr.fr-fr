---
title: Message LVM_GETHOVERTIME (commctrl. h)
description: Récupère la durée pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetHoverTime.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- LVM_GETHOVERTIME les contrôles de Windows de message
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
ms.openlocfilehash: 150a8eff54f8b3c27f0e7783ceda67af60c326e370d1a518d83e6bdd214fb529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920099"
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

## <a name="remarks"></a>Remarques

La durée de survol affecte uniquement les contrôles d’affichage de liste qui ont le style de vue de liste étendu [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)ou [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





