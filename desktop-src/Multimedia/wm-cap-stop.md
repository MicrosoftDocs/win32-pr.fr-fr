---
title: Message WM_CAP_STOP (VFW. h)
description: Le \_ message WM Cap \_ Stop arrête l’opération de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureStop.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- Message WM_CAP_STOP Windows Multimedia
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
ms.openlocfilehash: 9ded89ea8999fa2b29f576a6d047f5147d492bc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743540"
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

## <a name="remarks"></a>Notes

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

 

 





