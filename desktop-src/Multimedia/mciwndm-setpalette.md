---
title: Message MCIWNDM_SETPALETTE (VFW. h)
description: Le \_ message MCIWNDM SETPALETTE envoie un descripteur de palette au périphérique MCI associé à la fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetPalette.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- message MCIWNDM_SETPALETTE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e354082de4fc15f4179555a8b635b9426af90
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364327"
---
# <a name="mciwndm_setpalette-message"></a>\_Message MCIWNDM SETPALETTE

Le message **MCIWNDM \_ SETPALETTE** envoie un descripteur de palette au périphérique MCI associé à la fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hpal"></span><span id="HPAL"></span>*hpal*
</dt> <dd>

Handle de palette.

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

[**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





