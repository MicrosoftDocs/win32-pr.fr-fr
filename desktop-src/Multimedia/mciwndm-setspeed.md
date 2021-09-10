---
title: Message MCIWNDM_SETSPEED (VFW. h)
description: Le \_ message MCIWNDM SETSPEED définit la vitesse de lecture d’un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetSpeed.
ms.assetid: 7658dd25-dc68-4bd1-b995-df06b509be16
keywords:
- message MCIWNDM_SETSPEED Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282bb3a2e135b674605be55aaccaa455d30edbcc
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364331"
---
# <a name="mciwndm_setspeed-message"></a>\_Message MCIWNDM SETSPEED

Le message **MCIWNDM \_ SETSPEED** définit la vitesse de lecture d’un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) .


```C++
MCIWNDM_SETSPEED 
wParam = 0; 
lParam = (LPARAM) (UINT) iSpeed; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*
</dt> <dd>

Vitesse de lecture. Spécifiez 1000 pour la vitesse normale, des valeurs plus élevées pour des vitesses plus rapides et des valeurs plus petites pour des vitesses plus lentes.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
</dt> </dl>

 

 





