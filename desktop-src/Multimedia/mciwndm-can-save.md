---
title: Message MCIWNDM_CAN_SAVE (VFW. h)
description: Le MCIWNDM \_ peut \_ enregistrer un message détermine si un périphérique MCI peut enregistrer des données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanSave.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- Message MCIWNDM_CAN_SAVE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11b60b8a5d93ac80befc8beeb6665399efe44f1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464618"
---
# <a name="mciwndm_can_save-message"></a>MCIWNDM \_ peut \_ enregistrer le message

Le **MCIWNDM \_ peut \_ Enregistrer** un message détermine si un périphérique MCI peut enregistrer des données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) .


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** si l’appareil prend en charge l’enregistrement ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





