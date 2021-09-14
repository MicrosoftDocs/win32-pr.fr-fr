---
title: Message MCIWNDM_GETVOLUME (VFW. h)
description: Le \_ message MCIWNDM GETVOLUME récupère le paramètre de volume actuel d’un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetVolume.
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- message MCIWNDM_GETVOLUME Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa11fb13a56dda7cb83e3d6c98b4b66083e91b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009497"
---
# <a name="mciwndm_getvolume-message"></a>\_Message MCIWNDM GETVOLUME

Le message **MCIWNDM \_ GETVOLUME** récupère le paramètre de volume actuel d’un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne le paramètre de volume actuel. La valeur par défaut est 1000. Des valeurs plus élevées indiquent des volumes plus forts, les valeurs inférieures indiquent des volumes plus silencieux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 





