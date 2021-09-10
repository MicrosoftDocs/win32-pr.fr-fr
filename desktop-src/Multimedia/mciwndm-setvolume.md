---
title: Message MCIWNDM_SETVOLUME (VFW. h)
description: Le \_ message MCIWNDM SETVOLUME définit le niveau de volume d’un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetVolume.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- message MCIWNDM_SETVOLUME Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2215f8df3ea6f7b36b224318ebac68175ff9c265
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364335"
---
# <a name="mciwndm_setvolume-message"></a>\_Message MCIWNDM SETVOLUME

Le message **MCIWNDM \_ SETVOLUME** définit le niveau de volume d’un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*
</dt> <dd>

Nouveau niveau de volume. Spécifiez 1000 pour le niveau de volume normal. Spécifiez une valeur plus élevée pour un volume plus fort ou une valeur inférieure pour un volume plus silencieux.

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

[**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





