---
title: Message ICM_DRAW_FLUSH (VFW. h)
description: le \_ \_ message de vidage de dessin ICM notifie un pilote de rendu pour afficher le contenu de toutes les mémoires tampons d’image qui sont en attente de dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawFlush.
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- message ICM_DRAW_FLUSH Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364187"
---
# <a name="icm_draw_flush-message"></a>ICM \_ DESSINER le \_ message de vidage

le message de **\_ \_ vidage de dessin ICM** notifie un pilote de rendu pour afficher le contenu de toutes les mémoires tampons d’image qui sont en attente de dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) .


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

Ce message est utilisé uniquement par le matériel qui effectue sa propre décompression asynchrone, son minutage et son dessin.

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

 

 





