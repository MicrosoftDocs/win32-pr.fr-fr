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
ms.openlocfilehash: a919036ee38fdcf00f55c3d4044cd3f45bd13c82
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368044"
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

## <a name="requirements"></a>Spécifications



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

 

 





