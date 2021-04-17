---
title: Message ICM_DECOMPRESSEX_END (VFW. h)
description: Le \_ message de \_ fin DECOMPRESSEX ICM indique à un pilote de décompression vidéo de terminer la décompression et de libérer les ressources allouées pour la décompression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressExEnd.
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- Message ICM_DECOMPRESSEX_END Windows Multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509150"
---
# <a name="icm_decompressex_end-message"></a>\_Message de \_ fin DECOMPRESSEX ICM

Le message de **\_ \_ fin DECOMPRESSEX ICM** indique à un pilote de décompression vidéo de terminer la décompression et de libérer les ressources allouées pour la décompression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) .


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Le pilote libère toutes les ressources allouées pour le message de [**\_ \_ début DECOMPRESSEX ICM**](icm-decompressex-begin.md) .

[**ICM \_ Les \_**](icm-decompressex-begin.md) **\_ \_ terminaisons** DECOMPRESSEX Begin et ICM DECOMPRESSEX ne sont pas imbriquées. Si votre pilote reçoit **des \_ DECOMPRESSEX \_ ICM** avant que la décompression ne soit arrêtée avec l' **\_ \_ extrémité DECOMPRESSEX ICM**, il doit redémarrer la décompression avec les nouveaux paramètres.

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

 

 





