---
title: Message WM_CAP_GRAB_FRAME_NOSTOP (VFW. h)
description: Le \_ \_ message nostop de la trame de manipulation du capuchon WM \_ \_ remplit la mémoire tampon de trame avec un seul frame non compressé à partir du périphérique de capture et l’affiche.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- message WM_CAP_GRAB_FRAME_NOSTOP Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b81c581ad7e3913640271b32b18791ebf7b48ed09cd365af82ed263449f05471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622598"
---
# <a name="wm_cap_grab_frame_nostop-message"></a>\_ \_ \_ Message nostop de la trame de manipulation de l’embout WM \_

Le **message \_ \_ \_ \_ nostop de la trame de manipulation du capuchon WM** remplit la mémoire tampon de trame avec un seul frame non compressé à partir du périphérique de capture et l’affiche. Contrairement au message [**de \_ \_ \_ trame de manipulation de l’embout WM**](wm-cap-grab-frame.md) , l’état de la superposition ou de l’aperçu n’est pas modifié par ce message. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) .


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Pour plus d’informations sur l’installation des fonctions de rappel, consultez les messages d' [**\_ erreur WM Cap \_ Set \_ callback \_ Error**](wm-cap-set-callback-error.md) et [**WM \_ Cap \_ Set \_ callback \_ Frame**](wm-cap-set-callback-frame.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> <dt>

[Messages de capture vidéo](video-capture-messages.md)
</dt> </dl>

 

 





