---
title: Message WM_CAP_DRIVER_DISCONNECT (VFW. h)
description: Le \_ message de \_ déconnexion du pilote WM Cap \_ déconnecte un pilote de capture d’une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capDriverDisconnect.
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- message WM_CAP_DRIVER_DISCONNECT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6365366c6ea37b36734262d1d7a8412a7729406ff3fcc12e10ae9ba55d9ba84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803859"
---
# <a name="wm_cap_driver_disconnect-message"></a>\_Message de \_ déconnexion du pilote WM Cap \_

Le message de **\_ \_ \_ déconnexion du pilote WM Cap** déconnecte un pilote de capture d’une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) .


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la fenêtre de capture n’est pas connectée à un pilote de capture.

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

 

 





