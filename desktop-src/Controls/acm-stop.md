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
ms.openlocfilehash: 210936d102cdf7c55f25106ec5f6dc8e962c3af7679e6c5294ea10b6e833c8f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079403"
---
# <a name="acm_stop-message"></a>\_Message d’arrêt ACM

Arrête la diffusion d’un clip AVI dans un contrôle d’animation. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ arrêter l’animation**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





