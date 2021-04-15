---
title: Message WM_CAP_ABORT (VFW. h)
description: Le \_ message WM Cap \_ Abort arrête l’opération de capture.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- Message WM_CAP_ABORT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508538"
---
# <a name="wm_cap_abort-message"></a>\_Message WM Cap \_ Abort

Le message **WM \_ Cap \_ Abort** arrête l’opération de capture. Dans le cas de la capture de l’étape, les données d’image collectées jusqu’au point du message **WM \_ Cap \_ Abort** sont conservées dans le fichier de capture, mais l’audio n’est pas capturé. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) .


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

L’opération de capture doit donner l’utilisation de ce message.

Utilisez le message [**WM \_ Cap \_ Stop**](wm-cap-stop.md) pour interrompre la capture de l’étape à la position actuelle, puis capturez l’audio.

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

 

 





