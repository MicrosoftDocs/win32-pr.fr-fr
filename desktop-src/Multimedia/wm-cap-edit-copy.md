---
title: Message WM_CAP_EDIT_COPY (VFW. h)
description: Le \_ message WM Cap \_ Edit \_ Copy copie le contenu de la mémoire tampon de l’image vidéo et la palette associée dans le presse-papiers. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capEditCopy.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- message WM_CAP_EDIT_COPY Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367895"
---
# <a name="wm_cap_edit_copy-message"></a>Message WM- \_ \_ modifier la \_ copie

Le message **WM \_ Cap \_ Edit \_ Copy** copie le contenu de la mémoire tampon de l’image vidéo et la palette associée dans le presse-papiers. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) .


```C++
WM_CAP_EDIT_COPY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

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

 

 





