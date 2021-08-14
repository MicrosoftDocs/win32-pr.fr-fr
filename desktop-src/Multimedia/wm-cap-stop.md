---
title: Message WM_CAP_STOP (VFW. h)
description: Le \_ message WM Cap \_ Stop arrête l’opération de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureStop.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- message WM_CAP_STOP Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bceac7a821a42227a388de6ebc2b9ea548156ec80d1e5baba7f1e1ad708002d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369328"
---
# <a name="wm_cap_stop-message"></a>Message d’arrêt de l' \_ embout WM \_

Le message **WM \_ Cap \_ Stop** arrête l’opération de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) .

Dans la capture de frame de l’étape, les données d’image qui ont été collectées avant l’envoi de ce message sont conservées dans le fichier de capture. Une durée équivalente des données audio est également conservée dans le fichier de capture si la capture audio a été activée.


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

L’opération de capture doit donner l’utilisation de ce message. Utilisez le message [**WM \_ Cap \_ Abort**](wm-cap-abort.md) pour abandonner l’opération de capture en cours.

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

 

 





