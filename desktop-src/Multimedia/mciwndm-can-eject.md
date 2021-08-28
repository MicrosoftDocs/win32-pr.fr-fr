---
title: Message MCIWNDM_CAN_EJECT (VFW. h)
description: Le MCIWNDM \_ peut \_ éjecter le message pour déterminer si un périphérique MCI peut éjecter son support. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanEject.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- message MCIWNDM_CAN_EJECT Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fde4c9fec3972fe0e22b0a562454e1ef680e9ccae3851c272d28468fc2c91f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429669"
---
# <a name="mciwndm_can_eject-message"></a>MCIWNDM \_ peut \_ éjecter le message

Le **MCIWNDM \_ peut \_ éjecter** le message pour déterminer si un périphérique MCI peut éjecter son support. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) .


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** si l’appareil peut éjecter son média ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





