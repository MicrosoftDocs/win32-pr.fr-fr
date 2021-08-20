---
title: Message MCIWNDM_GETEND (VFW. h)
description: Le \_ message MCIWNDM GETEND récupère l’emplacement de la fin du contenu d’un périphérique ou d’un fichier MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetEnd.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- message MCIWNDM_GETEND Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880b1a464d671ca57e1955d4131776a999d1fb6bd8f17ad5d08139abc64a757b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137730"
---
# <a name="mciwndm_getend-message"></a>\_Message MCIWNDM GETEND

Le message **MCIWNDM \_ GETEND** récupère l’emplacement de la fin du contenu d’un périphérique ou d’un fichier MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne l’emplacement au format d’heure actuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





