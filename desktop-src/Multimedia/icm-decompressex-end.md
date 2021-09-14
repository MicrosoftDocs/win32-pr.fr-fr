---
title: Message ICM_DECOMPRESSEX_END (VFW. h)
description: le \_ message ICM DECOMPRESSEX \_ end indique à un pilote de décompression vidéo de terminer la décompression et de libérer les ressources allouées pour la décompression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressExEnd.
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- message ICM_DECOMPRESSEX_END Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e96f6a069e9ed2c9c52dc2f07f1ab4c5210ecd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021174"
---
# <a name="icm_decompressex_end-message"></a>ICM \_ DECOMPRESSEX \_ fin du message

le message **ICM \_ DECOMPRESSEX \_ end** indique à un pilote de décompression vidéo de terminer la décompression et de libérer les ressources allouées pour la décompression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) .


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Notes

le pilote libère toutes les ressources allouées pour le message [**ICM \_ DECOMPRESSEX \_ BEGIN**](icm-decompressex-begin.md) .

[**ICM \_ DECOMPRESSEX \_ BEGIN**](icm-decompressex-begin.md) et **ICM \_ DECOMPRESSEX \_ END** do not imbriquer. si votre pilote reçoit **ICM \_ DECOMPRESSEX \_ BEGIN** avant que la décompression ne soit arrêtée avec **ICM \_ \_ terminaison DECOMPRESSEX**, il doit redémarrer la décompression avec les nouveaux paramètres.

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

 

 





