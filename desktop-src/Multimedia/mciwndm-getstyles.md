---
title: Message MCIWNDM_GETSTYLES (VFW. h)
description: Le \_ message MCIWNDM GETSTYLES récupère les indicateurs qui spécifient les styles de fenêtre MCIWnd actuels utilisés par une fenêtre. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetStyles.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- message MCIWNDM_GETSTYLES Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036bd687c5d7828fade23994b9141488354added5ee38d38bafc9c5ce22a954c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783289"
---
# <a name="mciwndm_getstyles-message"></a>\_Message MCIWNDM GETSTYLES

Le message **MCIWNDM \_ GETSTYLES** récupère les indicateurs qui spécifient les styles de fenêtre MCIWnd actuels utilisés par une fenêtre. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur représentant les styles actuels de la fenêtre MCIWnd. La valeur de retour est l’opérateur or au niveau du bit des styles de fenêtre MCIWnd (indicateurs MCIWNDF).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





