---
title: Message MCIWNDM_CAN_RECORD (VFW. h)
description: Le MCIWNDM \_ peut \_ enregistrer un message détermine si un appareil MCI prend en charge l’enregistrement. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanRecord.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- message MCIWNDM_CAN_RECORD Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acbc9efa3ca973c12112a599d1202ad936107a9
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364236"
---
# <a name="mciwndm_can_record-message"></a>MCIWNDM \_ peut \_ enregistrer le message

Le **MCIWNDM \_ peut \_ Enregistrer** un message détermine si un appareil MCI prend en charge l’enregistrement. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) .


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** si l’appareil prend en charge l’enregistrement ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





