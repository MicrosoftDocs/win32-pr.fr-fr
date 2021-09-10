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
ms.openlocfilehash: 00ba54c9263e23fdd9830be892e4559ae3755c07
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364228"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





