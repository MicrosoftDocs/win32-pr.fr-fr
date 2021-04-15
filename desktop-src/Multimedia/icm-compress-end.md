---
title: Message ICM_COMPRESS_END (VFW. h)
description: Le message de fin de compression ICM \_ \_ indique à un pilote de compression vidéo d’arrêter la compression et les ressources gratuites allouées pour la compression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICCompressEnd.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- Message ICM_COMPRESS_END Windows Multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464835"
---
# <a name="icm_compress_end-message"></a>Message de fin de \_ compression ICM \_

Le message de **\_ \_ fin** de compression ICM indique à un pilote de compression vidéo d’arrêter la compression et les ressources gratuites allouées pour la compression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Notes

VCM enregistre les paramètres du message de début de la [**\_ \_ compression ICM**](icm-compress-begin.md) le plus récent. **ICM \_ Les \_** **\_ \_ terminaisons** de compression Begin et ICM ne sont pas imbriquées. Si votre pilote reçoit la compression ICM avant que la compression soit arrêtée avec la **\_ \_ terminaison** de compression ICM, il doit redémarrer la compression avec les nouveaux paramètres. **\_ \_**

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

 

 





