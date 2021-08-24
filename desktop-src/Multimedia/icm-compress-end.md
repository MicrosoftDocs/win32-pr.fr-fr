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
ms.openlocfilehash: 9c320190da37d286db1c20329a849ea09ac6d915087e9d3bdbb2333d31cec3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785039"
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

 

 





