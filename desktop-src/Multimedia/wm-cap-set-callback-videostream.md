---
title: Message WM_CAP_SET_CALLBACK_VIDEOSTREAM (VFW. h)
description: Le \_ message WM Cap \_ Set \_ callback \_ VIDEOSTREAM définit une fonction de rappel dans l’application.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- message WM_CAP_SET_CALLBACK_VIDEOSTREAM Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110741"
---
# <a name="wm_cap_set_callback_videostream-message"></a>\_ \_ \_ Message VIDEOSTREAM de rappel Set callback \_ de WM

Le message **WM \_ Cap \_ Set \_ callback \_ VIDEOSTREAM** définit une fonction de rappel dans l’application. AVICap appelle cette procédure lors de la capture en continu lorsqu’une mémoire tampon vidéo est remplie. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) .


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Pointeur vers la fonction de rappel de flux vidéo, de type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel de flux vidéo précédemment installée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu ou une session de capture de trame unique est en cours.

## <a name="remarks"></a>Notes

La fenêtre de capture appelle la fonction de rappel avant d’écrire le frame capturé sur le disque. Cela permet aux applications de modifier le frame si vous le souhaitez.

Si une fonction de rappel de flux vidéo est utilisée pour la capture en continu, la procédure doit être installée avant le démarrage de la session de capture et elle doit rester activée pendant toute la durée de la session. Elle peut être désactivée après la fin de la capture de streaming.

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

 

 





