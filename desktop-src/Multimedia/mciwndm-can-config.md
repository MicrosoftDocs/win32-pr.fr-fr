---
title: Message MCIWNDM_CAN_CONFIG (VFW. h)
description: Le \_ message MCIWNDM CAN \_ config détermine si un périphérique MCI peut afficher une boîte de dialogue de configuration. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanConfig.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- message MCIWNDM_CAN_CONFIG Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef5b8e4f8e1ab09f128b1294034bbb715c834c3e867f31bbaae0cb6bd620be5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525529"
---
# <a name="mciwndm_can_config-message"></a>MCIWNDM \_ peut \_ configurer un message

Le message **MCIWNDM \_ CAN \_ config** détermine si un périphérique MCI peut afficher une boîte de dialogue de configuration. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) .


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** si l’appareil prend en charge la configuration ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





