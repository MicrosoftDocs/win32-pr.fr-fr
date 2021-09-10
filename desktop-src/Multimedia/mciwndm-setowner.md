---
title: Message MCIWNDM_SETOWNER (VFW. h)
description: Le \_ message MCIWNDM de la conlocalité définit la fenêtre de réception des messages de notification associés à la fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetOwner.
ms.assetid: c2d0f9d5-bf60-4036-a613-65ba1ed83110
keywords:
- message MCIWNDM_SETOWNER Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETOWNER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3989632e83a65cda5e805bd91da3f502ca387d6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364324"
---
# <a name="mciwndm_setowner-message"></a>\_Message MCIWNDM

Le message MCIWNDM de la **\_ conlocalité** définit la fenêtre de réception des messages de notification associés à la fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .


```C++
MCIWNDM_SETOWNER 
wParam = (WPARAM) hwndP; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*
</dt> <dd>

Handle de la fenêtre pour recevoir les messages de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)
</dt> </dl>

 

 





