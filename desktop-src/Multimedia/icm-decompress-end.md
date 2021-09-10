---
title: Message ICM_DECOMPRESS_END (VFW. h)
description: le message de fin de décompression ICM \_ \_ indique à un pilote de décompression vidéo de terminer la décompression et de libérer les ressources allouées pour la décompression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressEnd.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- message ICM_DECOMPRESS_END Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364159"
---
# <a name="icm_decompress_end-message"></a>ICM \_ Décompresser le \_ message de fin

le message de **\_ \_ fin** de décompression ICM indique à un pilote de décompression vidéo de terminer la décompression et de libérer les ressources allouées pour la décompression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

le pilote doit libérer toutes les ressources allouées pour le message de [**\_ \_ début de décompression ICM**](icm-decompress-begin.md) .

[**ICM \_ le \_ début de la décompression**](icm-decompress-begin.md) ICM la fin de la **\_ décompression \_** ne sont pas imbriques. si votre pilote reçoit **ICM \_ décompresser \_ BEGIN** avant que la décompression ne s’arrête avec **ICM \_ \_ fin** de décompression, il doit redémarrer la décompression avec les nouveaux paramètres.

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

 

 





