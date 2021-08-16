---
title: Message MCIWNDM_NEW (VFW. h)
description: Le \_ nouveau message MCIWNDM crée un nouveau fichier pour l’appareil MCI actuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndNew.
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- message MCIWNDM_NEW Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bca9c03aff08c07f3ab1d8337547de776aeab5c6623a34ddaa71bfada0bca4f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783079"
---
# <a name="mciwndm_new-message"></a>MCIWNDM \_ un nouveau message

Le **\_ nouveau message MCIWNDM** crée un nouveau fichier pour l’appareil MCI actuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) .


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*Aid*
</dt> <dd>

Pointeur vers une mémoire tampon contenant le nom du périphérique MCI qui utilisera le fichier.

</dd> </dl>

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

[**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





