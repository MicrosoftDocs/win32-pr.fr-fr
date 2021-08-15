---
title: Message TBM_SETPOS (commctrl. h)
description: 'TBM_SETPOS message : définit la position logique actuelle du curseur dans un TrackBar.'
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ccd1cb35f8cde672c51baafe5623291e5449f90aa118eb36cb12152fe155385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078043"
---
# <a name="tbm_setpos-message"></a>\_Message TBM SetPos

Définit la position logique actuelle du curseur dans un TrackBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur de redessin. Si ce paramètre a la **valeur true**, le message redessine le contrôle à l’aide du curseur à la position donnée par *lParam*. Si ce paramètre a la **valeur false**, le message ne redessine pas le curseur à la nouvelle position. Notez que le message définit la valeur de la position du curseur (telle qu’elle est retournée par le message [**\_ GETPOS TBM**](tbm-getpos.md) ) quel que soit le paramètre *wParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Nouvelle position logique du curseur. Les positions logiques valides sont les valeurs entières de la plage de la plage de la barre de défilement minimale à la position maximale du curseur. Si cette valeur est en dehors de la plage maximale et minimale du contrôle, la position est définie sur la valeur maximale ou minimale.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





