---
title: Message WM_CAP_SINGLE_FRAME (VFW. h)
description: Le \_ message WM Cap \_ Single \_ Frame ajoute une image unique à un fichier de capture qui a été ouvert à l’aide du message d’ouverture du \_ \_ cadre unique WM Cap \_ \_ . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureSingleFrame.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- message WM_CAP_SINGLE_FRAME Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2080c8471849d42c2260c1f4133c996ef31e65e8a20591df531fbd24c19bc85c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891789"
---
# <a name="wm_cap_single_frame-message"></a>\_Message de \_ Frame unique WM Cap \_

Le message **WM \_ Cap \_ Single \_ Frame** ajoute une image unique à un fichier de capture qui a été ouvert à l’aide du message d' [**\_ \_ \_ \_ ouverture du cadre unique WM Cap**](wm-cap-single-frame-open.md) . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) .


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

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

 

 





