---
title: Message MCIWNDM_CAN_PLAY (VFW. h)
description: Le MCIWNDM \_ peut \_ lire le message détermine si un périphérique MCI peut lire un fichier de données ou un contenu d’un autre type. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanPlay.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- Message MCIWNDM_CAN_PLAY Windows Multimedia
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
ms.openlocfilehash: 043a0fc15260f7448df8d009a6b468616244269d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527579"
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

 

 





