---
title: Message ICM_DRAW_END (VFW. h)
description: Le \_ message ICM Draw \_ end indique à un pilote de rendu de décompresser l’image actuelle à l’écran et de libérer les ressources allouées pour la décompression et le dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawEnd.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- Message ICM_DRAW_END Windows Multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741964"
---
# <a name="icm_draw_end-message"></a>Message de fin de \_ dessin ICM \_

Le message **ICM \_ Draw \_ end** indique à un pilote de rendu de décompresser l’image actuelle à l’écran et de libérer les ressources allouées pour la décompression et le dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Les messages de **\_ \_ fin** de dessin [**ICM \_ \_**](icm-draw-begin.md) et ICM ne sont pas imbriqués. Si votre pilote reçoit **le \_ dessin \_ ICM, commencez** la décompression avec **les nouveaux paramètres \_ \_** pour arrêter la décompression.

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

 

 





