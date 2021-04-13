---
title: Message MCIWNDM_EJECT (VFW. h)
description: Le \_ message MCIWNDM EJECT envoie une commande à un périphérique MCI pour éjecter son support. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndEject.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- Message MCIWNDM_EJECT Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384123"
---
# <a name="mciwndm_eject-message"></a>MCIWNDM \_ éjecter le message

Le message **MCIWNDM \_ EJECT** envoie une commande à un périphérique MCI pour éjecter son support. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) .


```C++
MCIWNDM_EJECT 
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

[**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





