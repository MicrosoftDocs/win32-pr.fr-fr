---
title: Message WM_CAP_SEQUENCE_NOFILE (VFW. h)
description: Le \_ \_ \_ message d’inversion de séquence de l’embout WM lance la capture vidéo en continu sans écrire de données dans un fichier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureSequenceNoFile.
ms.assetid: 60cbcb62-3bfa-4182-a049-1e3cb2ede423
keywords:
- message WM_CAP_SEQUENCE_NOFILE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE_NOFILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a08f470989b8000e9757c1cb81924b875b5303
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368007"
---
# <a name="wm_cap_sequence_nofile-message"></a>\_ \_ Message nofile de séquence de l’embout WM \_

Le message d’inversion de séquence de l' **\_ embout \_ \_ WM** lance la capture vidéo en continu sans écrire de données dans un fichier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) .


```C++
WM_CAP_SEQUENCE_NOFILE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Ce message est utile conjointement avec les fonctions de rappel de flux vidéo ou Waveform-Audio qui permettent à votre application d’utiliser directement les données vidéo et audio.

Si vous souhaitez modifier les paramètres de contrôle de la capture en continu, utilisez le message [**\_ \_ \_ \_ d’installation de la séquence WM Cap Set**](wm-cap-set-sequence-setup.md) avant de démarrer la capture.

Par défaut, la fenêtre de capture ne permet pas à d’autres applications de continuer à s’exécuter pendant la capture. Pour remplacer cette valeur, affectez la **valeur true** au membre **fYield** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) ou installez une fonction de rappel yield.

Pendant la capture en continu, la fenêtre de capture peut éventuellement émettre des notifications pour votre application de types spécifiques de conditions. Pour installer des procédures de rappel pour ces notifications, utilisez les messages suivants :

-   [**erreur de rappel de l' \_ ensemble de connexions WM \_ \_ \_**](wm-cap-set-callback-error.md)
-   [**État de rappel de l' \_ ensemble de connexions WM \_ \_ \_**](wm-cap-set-callback-status.md)
-   [**\_jeu de \_ \_ rappels de la définition du jeu WM \_**](wm-cap-set-callback-yield.md)
-   [**WM \_ Cap \_ Set \_ callback \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**WM \_ Cap \_ Set \_ callback \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)

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

 

 





