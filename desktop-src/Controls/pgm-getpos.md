---
title: Message PGM_GETPOS (commctrl. h)
description: Récupère la position de défilement actuelle du contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ GetPos.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- PGM_GETPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106544174"
---
# <a name="pgm_getpos-message"></a>\_Message GETPOS PGM

Récupère la position de défilement actuelle du contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur INT qui contient la position de défilement actuelle, en pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





