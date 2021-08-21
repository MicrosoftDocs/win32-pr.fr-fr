---
title: Message MCIWNDM_GETREPEAT (VFW. h)
description: Le \_ message MCIWNDM GETREPEAT détermine si la lecture continue a été activée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetRepeat.
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- message MCIWNDM_GETREPEAT Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5045f56f2d189884e6d2dee978ec8800fa9c24c3ff01fc3fe93680b4ae7f53af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374196"
---
# <a name="mciwndm_getrepeat-message"></a>\_Message MCIWNDM GETREPEAT

Le message **MCIWNDM \_ GETREPEAT** détermine si la lecture continue a été activée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** si la lecture continue est activée ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





