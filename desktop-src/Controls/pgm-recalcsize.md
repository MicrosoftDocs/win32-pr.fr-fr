---
title: Message PGM_RECALCSIZE (commctrl. h)
description: Force le contrôle de pagineur à recalculer la taille de la fenêtre contenue. L’envoi de ce message entraîne l’envoi d’une \_ notification PGN CALCSIZE. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ RecalcSize.
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- PGM_RECALCSIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 099f17af0cc4edc79df01fcb03864cdbf2879ae75df701f30f32610a50ae884d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540539"
---
# <a name="pgm_recalcsize-message"></a>\_Message RECALCSIZE PGM

Force le contrôle de pagineur à recalculer la taille de la fenêtre contenue. L’envoi de ce message entraîne l’envoi d’une notification [PGN \_ CALCSIZE](pgn-calcsize.md) . Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





