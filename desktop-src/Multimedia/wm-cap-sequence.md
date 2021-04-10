---
title: Message WM_CAP_SEQUENCE (VFW. h)
description: Le message de séquence de l' \_ embout WM \_ initie la diffusion vidéo et la capture audio dans un fichier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureSequence.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- Message WM_CAP_SEQUENCE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ef945510d0d71f1aa0e0cb5827288a613f5991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942271"
---
# <a name="wm_cap_sequence-message"></a>Message de séquence de l' \_ embout WM \_

Le message de **\_ \_ séquence de l’embout WM** initie la diffusion vidéo et la capture audio dans un fichier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) .


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.

## <a name="remarks"></a>Notes

Si vous souhaitez modifier les paramètres de contrôle de la capture en continu, utilisez le message [**\_ \_ \_ \_ d’installation de la séquence WM Cap Set**](wm-cap-set-sequence-setup.md) avant de démarrer la capture.

Par défaut, la fenêtre de capture ne permet pas à d’autres applications de continuer à s’exécuter pendant la capture. Pour remplacer cette valeur, affectez la **valeur true** au membre **fYield** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) ou installez une fonction de rappel yield.

Pendant la capture en continu, la fenêtre de capture peut éventuellement émettre des notifications pour votre application de types spécifiques de conditions. Pour installer des procédures de rappel pour ces notifications, utilisez les messages suivants :

-   [**erreur de rappel de l' \_ ensemble de connexions WM \_ \_ \_**](wm-cap-set-callback-error.md)
-   [**État de rappel de l' \_ ensemble de connexions WM \_ \_ \_**](wm-cap-set-callback-status.md)
-   [**\_jeu de \_ \_ rappels de la définition du jeu WM \_**](wm-cap-set-callback-yield.md)
-   [**WM \_ Cap \_ Set \_ callback \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**WM \_ Cap \_ Set \_ callback \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)

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

 

 





