---
title: Message ICM_DRAW_STOP (VFW. h)
description: le \_ message d' \_ arrêt de ICM trace informe un pilote de rendu d’arrêter son horloge interne pour le minutage des frames de dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawStop.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- message ICM_DRAW_STOP Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364203"
---
# <a name="icm_draw_stop-message"></a>ICM \_ DESSINER un \_ message d’arrêt

le message d' **\_ \_ arrêt de ICM trace** informe un pilote de rendu d’arrêter son horloge interne pour le minutage des frames de dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) .


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Ce message est utilisé par le matériel qui effectue sa propre décompression, son minutage et son dessin asynchrones.

## <a name="requirements"></a>Spécifications



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

 

 





