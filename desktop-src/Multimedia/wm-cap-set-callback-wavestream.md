---
title: Message WM_CAP_SET_CALLBACK_WAVESTREAM (VFW. h)
description: Le \_ message de \_ rappel de la valeur du paramètre WM Cap Set \_ \_ définit une fonction de rappel dans l’application.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- message WM_CAP_SET_CALLBACK_WAVESTREAM Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36abc7848de082e033cfc25d4f15d90c86cf3b2
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367996"
---
# <a name="wm_cap_set_callback_wavestream-message"></a>\_ \_ \_ Message WAVESTREAM de rappel \_ défini par WM Cap

Le message de rappel de la **\_ valeur du paramètre WM Cap \_ Set \_ \_** définit une fonction de rappel dans l’application. AVICap appelle cette procédure lors de la capture en continu lorsqu’une nouvelle mémoire tampon audio est disponible. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) .


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Pointeur vers la fonction de rappel de flux Wave, de type [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback). Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel de flux Wave précédemment installée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu ou une session de capture de trame unique est en cours.

## <a name="remarks"></a>Remarques

La fenêtre de capture appelle la procédure avant d’écrire la mémoire tampon audio sur le disque. Cela permet aux applications de modifier la mémoire tampon audio si vous le souhaitez.

Si une fonction de rappel de flux Wave est utilisée, elle doit être installée avant le démarrage de la session de capture et elle doit rester activée pendant toute la durée de la session. Elle peut être désactivée après la fin de la capture de streaming.

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

 

 





