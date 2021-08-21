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
ms.openlocfilehash: 7b4986224fd23898ef33f8fdda4c12d17880a8bc42441b29cd1865fb7fdfa687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525229"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





