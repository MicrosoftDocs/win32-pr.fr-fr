---
title: Message WM_CAP_SET_PREVIEWRATE (VFW. h)
description: Le \_ message WM Cap \_ Set \_ PREVIEWRATE définit la fréquence d’affichage des frames en mode aperçu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capPreviewRate.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- Message WM_CAP_SET_PREVIEWRATE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942794"
---
# <a name="wm_cap_set_previewrate-message"></a>\_Message PREVIEWRATE de l’ensemble de connexions WM \_ \_

Le message **WM \_ Cap \_ Set \_ PREVIEWRATE** définit la fréquence d’affichage des frames en mode aperçu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) .


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*
</dt> <dd>

Vitesse, en millisecondes, à laquelle les nouveaux frames sont capturés et affichés.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la fenêtre de capture n’est pas connectée à un pilote de capture.

## <a name="remarks"></a>Notes

Le mode aperçu utilise des ressources processeur importantes. Les applications peuvent désactiver l’aperçu ou réduire le taux d’aperçu lorsqu’une autre application a le focus. Pendant la capture vidéo en continu, la tâche d’aperçu est moins prioritaire que l’écriture d’images sur le disque, et les images d’aperçu ne sont affichées que si aucune autre mémoire tampon n’est disponible pour l’écriture.

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

 

 





