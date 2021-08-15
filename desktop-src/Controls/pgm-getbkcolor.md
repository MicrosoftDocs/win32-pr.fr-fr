---
title: Message PGM_GETBKCOLOR (commctrl. h)
description: Récupère la couleur d’arrière-plan actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ GetBkColor.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- PGM_GETBKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff3ee3a4be09a948654d337a47eecdd2a7b15d16b0602016aa99500cd1c3728c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985939"
---
# <a name="pgm_getbkcolor-message"></a>\_Message GETBKCOLOR PGM

Récupère la couleur d’arrière-plan actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **COLORREF** qui contient la couleur d’arrière-plan actuelle.

## <a name="remarks"></a>Remarques

Par défaut, le contrôle de pagineur utilise la couleur de la face du bouton système comme couleur d’arrière-plan. Il s’agit de la même couleur que celle qui peut être récupérée en appelant [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) avec la couleur \_ BTNFACE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

