---
title: Message MCIWNDM_PLAYREVERSE (VFW. h)
description: Le \_ message MCIWNDM PLAYREVERSE lit le contenu actuel dans le sens inverse, en commençant à la position actuelle et en se terminant au début du contenu ou jusqu’à ce qu’une autre commande arrête la lecture.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- message MCIWNDM_PLAYREVERSE Windows Multimedia
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
ms.openlocfilehash: f5664ea53f73745648e668a78a6dc5f6da28a9cb27d54b96fced09523f655ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037969"
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

 

 





