---
title: Message MCIWNDM_GETZOOM (VFW. h)
description: Le \_ message MCIWNDM GETZOOM récupère la valeur de zoom actuelle utilisée par un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetZoom.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- message MCIWNDM_GETZOOM Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c247230ffe6269f77b906d874a4cf82a21ed8d3388ffa18193417603e45fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374140"
---
# <a name="mciwndm_getzoom-message"></a>\_Message MCIWNDM GETZOOM

Le message **MCIWNDM \_ GETZOOM** récupère la valeur de zoom actuelle utilisée par un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne les valeurs les plus récentes utilisées avec [**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md).

## <a name="remarks"></a>Remarques

Une valeur de retour de 100 indique que l’image n’est pas zoomée. Une valeur de 200 indique que l’image est agrandie à deux fois sa taille d’origine. Une valeur de 50 indique que l’image est réduite à la moitié de sa taille d’origine.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md)
</dt> </dl>

 

 





