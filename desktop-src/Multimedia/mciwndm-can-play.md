---
title: Message MCIWNDM_CAN_PLAY (VFW. h)
description: Le MCIWNDM \_ peut \_ lire le message détermine si un périphérique MCI peut lire un fichier de données ou un contenu d’un autre type. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanPlay.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- message MCIWNDM_CAN_PLAY Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84d067b01dbce8aaab7c78ab24c3d11fc5d4a3a19b9bfdb663eb653ebc0c553c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374241"
---
# <a name="mciwndm_can_play-message"></a>MCIWNDM \_ peut \_ lire le message

Le **MCIWNDM \_ peut \_ lire** le message détermine si un périphérique MCI peut lire un fichier de données ou un contenu d’un autre type. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) .


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** si l’appareil prend en charge la diffusion des données ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





