---
title: Message WM_CAP_SET_CALLBACK_FRAME (VFW. h)
description: Le \_ message WM Cap \_ Set \_ callback \_ Frame définit une fonction de rappel d’aperçu dans l’application. AVICap appelle cette procédure lorsque la fenêtre de capture capture des images d’aperçu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetCallbackOnFrame.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- message WM_CAP_SET_CALLBACK_FRAME Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85321483639135db31750cacf76cc5f0dc4ad42e96474efa1dc17ac84ba4a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369507"
---
# <a name="wm_cap_set_callback_frame-message"></a>\_Message de \_ \_ \_ trame de rappel de la définition de l’embout WM

Le message **WM \_ Cap \_ Set \_ callback \_ Frame** définit une fonction de rappel d’aperçu dans l’application. AVICap appelle cette procédure lorsque la fenêtre de capture capture des images d’aperçu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Pointeur vers la fonction de rappel d’aperçu, de type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel précédemment installée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu ou une session de capture de trame unique est en cours.

## <a name="remarks"></a>Remarques

La fenêtre de capture appelle la fonction de rappel avant d’afficher des images d’aperçu. Cela permet à une application de modifier le frame si vous le souhaitez. Cette fonction de rappel n’est pas utilisée pendant la capture vidéo en continu.

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

 

 





