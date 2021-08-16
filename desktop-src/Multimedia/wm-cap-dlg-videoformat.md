---
title: Message WM_CAP_DLG_VIDEOFORMAT (VFW. h)
description: Le \_ message WM Cap \_ DLG \_ VIDEOFORMAT affiche une boîte de dialogue dans laquelle l’utilisateur peut sélectionner le format vidéo.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- message WM_CAP_DLG_VIDEOFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaa58e99c6a07db9109a0b1a6dae25de8abd46fef2631eb539961de16455ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135398"
---
# <a name="wm_cap_dlg_videoformat-message"></a>\_Message WM Cap \_ DLG \_ VIDEOFORMAT

Le message **WM \_ Cap \_ DLG \_ VIDEOFORMAT** affiche une boîte de dialogue dans laquelle l’utilisateur peut sélectionner le format vidéo. La boîte de dialogue Format vidéo peut être utilisée pour sélectionner les dimensions d’image, la profondeur de bit et les options de compression matérielle. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) .


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Une fois ce message retourné, les applications devront peut-être mettre à jour la structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) car l’utilisateur a peut-être modifié les dimensions de l’image.

La boîte de dialogue Format vidéo est unique pour chaque pilote de capture. Certains pilotes de capture peuvent ne pas prendre en charge la boîte de dialogue Format vidéo. Les applications peuvent déterminer si le pilote de capture prend en charge ce message en vérifiant le membre **fHasDlgVideoFormat** de [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).

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

 

 





