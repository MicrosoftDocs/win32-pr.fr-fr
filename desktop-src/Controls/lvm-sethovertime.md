---
title: Message LVM_SETHOVERTIME (commctrl. h)
description: Définit la durée pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetHoverTime.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- LVM_SETHOVERTIME les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3aecd3c0d48cddc2cbaae49e7e888f91a985575
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312705"
---
# <a name="lvm_sethovertime-message"></a>\_Message SETHOVERTIME LVM

Définit la durée pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Nouvelle durée, en millisecondes, pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné. Si cette valeur est (**DWORD**)-1, la durée de survol est définie sur la durée de pointage par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la durée de pointage précédente.

## <a name="remarks"></a>Remarques

La durée de survol affecte uniquement les contrôles d’affichage de liste qui ont le style de vue de liste étendu [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)ou [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





