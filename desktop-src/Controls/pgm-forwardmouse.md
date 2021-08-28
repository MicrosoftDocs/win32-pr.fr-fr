---
title: Message PGM_FORWARDMOUSE (commctrl. h)
description: Active ou désactive le transfert de la souris pour le contrôle de pagineur. Lorsque le transfert de souris est activé, le contrôle de pagineur transfère les \_ messages de la souris WM à la fenêtre contenue. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ ForwardMouse.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- PGM_FORWARDMOUSE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705b63ad39faea86e1f38a5b59dc73c6fc12f1e19fc17d0619c9a4b3dd5c6d26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046969"
---
# <a name="pgm_forwardmouse-message"></a>\_Message FORWARDMOUSE PGM

Active ou désactive le transfert de la souris pour le contrôle de pagineur. Lorsque le transfert de souris est activé, le contrôle de pagineur transfère les messages de la souris [**WM \_**](/windows/desktop/inputdev/wm-mousemove) à la fenêtre contenue. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur **booléenne** qui détermine si le transfert de souris est activé ou désactivé. Si cette valeur est différente de zéro, le transfert de souris est activé. Si cette valeur est égale à zéro, le transfert de la souris est désactivé.

</dd> <dt>

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



 

