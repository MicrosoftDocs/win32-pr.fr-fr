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
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117681"
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

## <a name="return-value"></a>Valeur de retour

La valeur de retour n’est pas utilisée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

