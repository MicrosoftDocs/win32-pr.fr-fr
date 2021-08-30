---
title: Message ICM_DRAW_STOP_PLAY (VFW. h)
description: le \_ message ICM DRAW \_ STOP \_ PLAY avertit un pilote de rendu quand une opération de lecture est terminée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawStopPlay.
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- message ICM_DRAW_STOP_PLAY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb5ed2d437a3abc0d24972ee739905a72d2333509e7213973bab9459c7c947a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784979"
---
# <a name="icm_draw_stop_play-message"></a>ICM \_ DESSINER le message d’arrêt de la \_ \_ lecture

le message **ICM \_ DRAW \_ STOP \_ PLAY** avertit un pilote de rendu quand une opération de lecture est terminée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) .


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Utilisez ce message lorsque l’opération de lecture est terminée. utilisez le [**ICM \_ dessiner \_**](icm-draw-stop.md) le message d’arrêt pour terminer le minutage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de compression vidéo](video-compression-manager.md)
</dt> <dt>

[Messages de compression vidéo](video-compression-messages.md)
</dt> </dl>

 

 





