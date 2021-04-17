---
title: Message WM_CAP_GRAB_FRAME (VFW. h)
description: Le \_ message de \_ Frame de capture du capuchon WM \_ récupère et affiche une image unique du pilote de capture. Après la capture, la superposition et l’aperçu sont désactivés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capGrabFrame.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- Message WM_CAP_GRAB_FRAME Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd91ce767ad86ddac002bb216420b604883d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465666"
---
# <a name="wm_cap_grab_frame-message"></a>\_Message du \_ Frame de capture du capuchon WM \_

Le message de **\_ \_ \_ Frame** de capture du capuchon WM récupère et affiche une image unique du pilote de capture. Après la capture, la superposition et l’aperçu sont désactivés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) .


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Pour plus d’informations sur l’installation des fonctions de rappel, consultez les messages d' [**\_ erreur WM Cap \_ Set \_ callback \_ Error**](wm-cap-set-callback-error.md) et [**WM \_ Cap \_ Set \_ callback \_ Frame**](wm-cap-set-callback-frame.md) .

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

 

 





