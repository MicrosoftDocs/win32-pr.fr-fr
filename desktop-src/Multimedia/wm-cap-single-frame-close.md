---
title: Message WM_CAP_SINGLE_FRAME_CLOSE (VFW. h)
description: Le \_ message de \_ fermeture de frame unique WM capuchon \_ \_ ferme le fichier de capture ouvert par le \_ message d’ouverture du \_ cadre unique WM Cap \_ \_ . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureSingleFrameClose.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- message WM_CAP_SINGLE_FRAME_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35523476dde1c74c4a20447d7c46d5eafc5e529
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368052"
---
# <a name="wm_cap_single_frame_close-message"></a>\_Message de \_ \_ fermeture de frame unique WM Cap \_

Le message de **\_ \_ \_ \_ fermeture de frame unique WM capuchon** ferme le fichier de capture ouvert par le message d' [**\_ \_ \_ \_ ouverture du cadre unique WM Cap**](wm-cap-single-frame-open.md) . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) .


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Pour plus d’informations sur l’installation des fonctions de rappel, consultez les messages d' [**\_ erreur WM Cap \_ Set \_ callback \_ Error**](wm-cap-set-callback-error.md) et [**WM \_ Cap \_ Set \_ callback \_ Frame**](wm-cap-set-callback-frame.md) .

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

 

 





