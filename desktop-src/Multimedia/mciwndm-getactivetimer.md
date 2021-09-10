---
title: Message MCIWNDM_GETACTIVETIMER (VFW. h)
description: Le \_ message MCIWNDM GETACTIVETIMER récupère la période de mise à jour utilisée lorsque la fenêtre MCIWnd est la fenêtre active. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetActiveTimer.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- message MCIWNDM_GETACTIVETIMER Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364244"
---
# <a name="mciwndm_getactivetimer-message"></a>\_Message MCIWNDM GETACTIVETIMER

Le message **MCIWNDM \_ GETACTIVETIMER** récupère la période de mise à jour utilisée lorsque la fenêtre MCIWnd est la fenêtre active. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la période de mise à jour en millisecondes. La valeur par défaut est 500 millisecondes.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





