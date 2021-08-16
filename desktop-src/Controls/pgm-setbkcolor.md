---
title: Message PGM_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ SetBkColor.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- PGM_SETBKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d727bf401fae3b8c58b96fe8b5190a3ad427abb40b0478d59de087add553ddf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830180"
---
# <a name="pgm_setbkcolor-message"></a>\_Message SETBKCOLOR PGM

Définit la couleur d’arrière-plan actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur **COLORREF** qui contient la nouvelle couleur d’arrière-plan du contrôle de pagineur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **COLORREF** qui contient la couleur d’arrière-plan précédente.

## <a name="remarks"></a>Remarques

Par défaut, le contrôle de pagineur utilise la couleur de la face du bouton système comme couleur d’arrière-plan. Il s’agit de la même couleur que celle qui peut être récupérée en appelant [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) avec la couleur \_ BTNFACE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

