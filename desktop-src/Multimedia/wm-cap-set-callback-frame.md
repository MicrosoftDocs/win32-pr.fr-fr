---
title: Message WM_CAP_SET_CALLBACK_FRAME (VFW. h)
description: Le \_ message WM Cap \_ Set \_ callback \_ Frame définit une fonction de rappel d’aperçu dans l’application. AVICap appelle cette procédure lorsque la fenêtre de capture capture des images d’aperçu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetCallbackOnFrame.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- Message WM_CAP_SET_CALLBACK_FRAME Windows Multimedia
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
ms.openlocfilehash: b91c2f30ac0875e2f45592d3aa7e0a3ce9c296b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536292"
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

## <a name="remarks"></a>Notes

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

 

 





