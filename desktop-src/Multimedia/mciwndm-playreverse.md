---
title: Message MCIWNDM_PLAYREVERSE (VFW. h)
description: Le \_ message MCIWNDM PLAYREVERSE lit le contenu actuel dans le sens inverse, en commençant à la position actuelle et en se terminant au début du contenu ou jusqu’à ce qu’une autre commande arrête la lecture.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- Message MCIWNDM_PLAYREVERSE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102840"
---
# <a name="mciwndm_playreverse-message"></a>\_Message MCIWNDM PLAYREVERSE

Le message **MCIWNDM \_ PLAYREVERSE** lit le contenu actuel dans le sens inverse, en commençant à la position actuelle et en se terminant au début du contenu ou jusqu’à ce qu’une autre commande arrête la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





