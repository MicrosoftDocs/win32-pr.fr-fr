---
title: Message ICM_DRAW_STOP_PLAY (VFW. h)
description: Le \_ message ICM Draw \_ Stop \_ Play avertit un pilote de rendu quand une opération de lecture est terminée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawStopPlay.
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- Message ICM_DRAW_STOP_PLAY Windows Multimedia
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
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106552"
---
# <a name="icm_draw_stop_play-message"></a>Message d’arrêt de la \_ \_ \_ lecture ICM

Le message **ICM \_ Draw \_ Stop \_ Play** avertit un pilote de rendu quand une opération de lecture est terminée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) .


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Utilisez ce message lorsque l’opération de lecture est terminée. Utilisez le message [**ICM \_ Draw \_ Stop**](icm-draw-stop.md) pour terminer le minutage.

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

 

 





