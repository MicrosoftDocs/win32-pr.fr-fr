---
title: Message LVM_GETHOTCURSOR (commctrl. h)
description: Récupère la valeur HCURSOR utilisée lorsque le pointeur se trouve sur un élément alors que la sélection active est activée. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetHotCursor.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- LVM_GETHOTCURSOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5703d252d239124b78656c4a5991efdecb2107552fb6e2ab0f87701af4e18d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540799"
---
# <a name="lvm_gethotcursor-message"></a>\_Message GETHOTCURSOR LVM

Récupère la valeur HCURSOR utilisée lorsque le pointeur se trouve sur un élément alors que la sélection active est activée. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur HCURSOR qui est le handle du curseur que le contrôle d’affichage de liste utilise lorsque la sélection active est activée.

## <a name="remarks"></a>Remarques

Un contrôle List-View utilise le suivi réactif et la sélection au pointage lorsque le style [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) est défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





