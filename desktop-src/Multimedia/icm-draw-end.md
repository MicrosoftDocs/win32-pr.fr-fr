---
title: Message ICM_DRAW_END (VFW. h)
description: le \_ message ICM DRAW \_ END indique à un pilote de rendu de décompresser l’image actuelle à l’écran et de libérer les ressources allouées pour la décompression et le dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawEnd.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- message ICM_DRAW_END Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364172"
---
# <a name="icm_draw_end-message"></a>ICM \_ DESSINER le \_ message de fin

le message **ICM \_ DRAW \_ END** indique à un pilote de rendu de décompresser l’image actuelle à l’écran et de libérer les ressources allouées pour la décompression et le dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

le [**ICM \_ dessiner \_ commencer**](icm-draw-begin.md) et **ICM \_ dessiner \_** les messages de fin ne sont pas imbriqués. si votre pilote reçoit **ICM \_ \_ commencer** avant que la décompression ne s’arrête avec **ICM \_ dessiner \_**, il doit redémarrer la décompression avec les nouveaux paramètres.

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

 

 





