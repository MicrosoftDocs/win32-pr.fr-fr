---
title: Message MCIWNDM_GETINACTIVETIMER (VFW. h)
description: Le \_ message MCIWNDM GETINACTIVETIMER récupère la période de mise à jour utilisée lorsque la fenêtre MCIWnd est la fenêtre inactive. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetInactiveTimer.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- message MCIWNDM_GETINACTIVETIMER Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec8de85796139b98e76d631a9386493752dad9942241069a7f1a5ab535fab72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038079"
---
# <a name="mciwndm_getinactivetimer-message"></a>\_Message MCIWNDM GETINACTIVETIMER

Le message **MCIWNDM \_ GETINACTIVETIMER** récupère la période de mise à jour utilisée lorsque la fenêtre MCIWnd est la fenêtre inactive. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la période de mise à jour, en millisecondes. La valeur par défaut est 2000 millisecondes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





