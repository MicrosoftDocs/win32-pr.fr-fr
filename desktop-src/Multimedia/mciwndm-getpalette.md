---
title: Message MCIWNDM_GETPALETTE (VFW. h)
description: Le \_ message MCIWNDM GETPALETTE récupère un descripteur de la palette utilisée par un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetPalette.
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- message MCIWNDM_GETPALETTE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faec3dd5d9c401d943fbc55ca58e452d3fb25497
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364267"
---
# <a name="mciwndm_getpalette-message"></a>\_Message MCIWNDM GETPALETTE

Le message **MCIWNDM \_ GETPALETTE** récupère un descripteur de la palette utilisée par un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) .


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne le handle de la palette en cas de réussite.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 





