---
title: Message PGM_GETBORDER (commctrl. h)
description: Récupère la taille de bordure actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ GetBorder.
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- PGM_GETBORDER les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148b3d840548116d3082e27b5a760650c5802bdb2c6dbc1fc7c94f1df3a3d5b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046859"
---
# <a name="pgm_getborder-message"></a>\_Message GETBORDER PGM

Récupère la taille de bordure actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur INT qui contient la taille actuelle de la bordure, en pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETBORDER PGM**](pgm-setborder.md)
</dt> </dl>

 

 





