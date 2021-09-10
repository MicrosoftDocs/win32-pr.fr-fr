---
title: Message MCIWNDM_GETDEVICEID (VFW. h)
description: Le \_ message MCIWNDM GETDEVICEID récupère l’identificateur du périphérique MCI actuellement ouvert à utiliser avec la fonction mciSendCommand. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetDeviceID.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- message MCIWNDM_GETDEVICEID Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364252"
---
# <a name="mciwndm_getdeviceid-message"></a>\_Message MCIWNDM GETDEVICEID

Le message **MCIWNDM \_ GETDEVICEID** récupère l’identificateur du périphérique MCI actuellement ouvert à utiliser avec la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne l’identificateur de l’appareil.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 

