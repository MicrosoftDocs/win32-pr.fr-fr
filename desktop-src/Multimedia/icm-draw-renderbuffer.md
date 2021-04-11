---
title: Message ICM_DRAW_RENDERBUFFER (VFW. h)
description: Le \_ message RENDERBUFFER de dessin ICM \_ indique à un pilote de rendu de dessiner les frames qui lui ont été transmis. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawRenderBuffer.
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- Message ICM_DRAW_RENDERBUFFER Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942595"
---
# <a name="icm_draw_renderbuffer-message"></a>\_Message RENDERBUFFER de dessin ICM \_

Le **message \_ \_ RENDERBUFFER de dessin ICM** indique à un pilote de rendu de dessiner les frames qui lui ont été transmis. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) .


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Utilisez ce message avec un matériel qui effectue sa propre décompression, son minutage et son dessin asynchrones.

Ce message est généralement utilisé pour effectuer une opération de recherche lorsque le pilote doit être spécifiquement invité à afficher chaque image vidéo qui lui est transmise au lieu de lancer une séquence de trames vidéo.

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

 

 





