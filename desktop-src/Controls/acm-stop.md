---
title: Message ACM_STOP (commctrl. h)
description: Arrête la diffusion d’un clip AVI dans un contrôle d’animation. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro arrêter l’animation.
ms.assetid: ba39a579-665e-4d45-8f1f-f190acd76db7
keywords:
- ACM_STOP les contrôles de Windows de message
topic_type:
- apiref
api_name:
- ACM_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81cfc92ac2778ae559fcd9fb8db2b0cd7bb866
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010174"
---
# <a name="acm_stop-message"></a>\_Message d’arrêt ACM

Arrête la diffusion d’un clip AVI dans un contrôle d’animation. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ arrêter l’animation**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





