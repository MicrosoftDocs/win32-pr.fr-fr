---
title: Message MCIWNDM_GETLENGTH (VFW. h)
description: Le \_ message MCIWNDM GETLENGTH récupère la longueur du contenu ou du fichier actuellement utilisé par un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetLength.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- message MCIWNDM_GETLENGTH Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334d9a4a62171a62cbd0fc914be2d9a81ed901eab6d3893170cb8dabd2426a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374186"
---
# <a name="mciwndm_getlength-message"></a>\_Message MCIWNDM GETLENGTH

Le message **MCIWNDM \_ GETLENGTH** récupère la longueur du contenu ou du fichier actuellement utilisé par un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la longueur. Les unités de la longueur dépendent du format d’heure actuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





