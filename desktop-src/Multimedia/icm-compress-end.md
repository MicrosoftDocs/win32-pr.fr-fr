---
title: Message ICM_COMPRESS_END (VFW. h)
description: le \_ message ICM compresser la \_ fin indique à un pilote de compression vidéo d’arrêter la compression et les ressources gratuites allouées à la compression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICCompressEnd.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- message ICM_COMPRESS_END Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364107"
---
# <a name="icm_compress_end-message"></a>ICM \_ Compresser le \_ message de fin

le message **ICM \_ compresser la \_ fin** indique à un pilote de compression vidéo d’arrêter la compression et les ressources gratuites allouées à la compression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

VCM enregistre les paramètres du message de [**début de \_ compression \_ ICM**](icm-compress-begin.md) le plus récent. **ICM \_ les \_** **\_ \_ terminaisons** de compression BEGIN et ICM ne sont pas imbriquées. si votre pilote reçoit **ICM la compression \_ \_ commencent** avant l’arrêt de la compression avec **ICM \_ \_ fin** de compression, il doit redémarrer la compression avec les nouveaux paramètres.

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

 

 





