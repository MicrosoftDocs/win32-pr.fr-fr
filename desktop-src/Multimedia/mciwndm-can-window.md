---
title: Message MCIWNDM_CAN_WINDOW (VFW. h)
description: Le \_ message de fenêtre MCIWNDM peut \_ déterminer si un périphérique MCI prend en charge les commandes MCI orientées fenêtre. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanWindow.
ms.assetid: bf89c096-1272-441e-9334-2b4215dbc979
keywords:
- message MCIWNDM_CAN_WINDOW Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26db92a07437f10295c2670e035950be5a56813aa6bb4c6252cfe35ef502f77c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038149"
---
# <a name="mciwndm_can_window-message"></a>MCIWNDM \_ peut être un \_ message de fenêtre

Le message de **\_ \_ fenêtre MCIWNDM peut** déterminer si un périphérique MCI prend en charge les commandes MCI orientées fenêtre. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) .


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** si l’appareil prend en charge les commandes MCI orientées fenêtre ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)
</dt> </dl>

 

 





