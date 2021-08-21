---
title: Message WM_CAP_SINGLE_FRAME_OPEN (VFW. h)
description: Le \_ \_ \_ message d’ouverture du frame unique WM Cap \_ ouvre le fichier de capture pour la capture d’une seule image. Toutes les informations précédentes du fichier de capture sont remplacées. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureSingleFrameOpen.
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- message WM_CAP_SINGLE_FRAME_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a58df70bea8971e10a769efbbc98220c46897ff6979e66ab45ae8f2ba81b971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134834"
---
# <a name="wm_cap_single_frame_open-message"></a>\_Message d' \_ ouverture d’un frame unique WM Cap \_ \_

Le message d' **\_ \_ \_ \_ ouverture du frame unique WM Cap** ouvre le fichier de capture pour la capture d’une seule image. Toutes les informations précédentes du fichier de capture sont remplacées. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) .


```C++
WM_CAP_SINGLE_FRAME_OPEN 
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

 

 





