---
title: Message MM_JOY2ZMOVE (mmsystem. h)
description: Le \_ message JOY2ZMOVE mm notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID2 que la position de la manette de jeu sur l’axe z a changé.
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- Message MM_JOY2ZMOVE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY2ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517337"
---
# <a name="mm_joy2zmove-message"></a>MM \_ message JOY2ZMOVE

Le **message \_ JOY2ZMOVE mm** notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID2 que la position de la manette de jeu sur l’axe z a changé.


```C++
MM_JOY2ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifie les boutons qui sont enfoncés. Il peut s’agir d’une ou plusieurs des valeurs suivantes.



| Condition requise | Valeur |
|--------------|------------------------------------|
| JOIE, \_ Button1 | Le premier bouton de la manette de jeu est enfoncé.  |
| BONHEUR \_ button2 | Le second bouton de la manette de jeu est enfoncé. |
| BONHEUR \_ BUTTON3 | Le bouton de la manette de jeu est enfoncé.  |
| JOIE \_ BUTTON4 | Le bouton de la quatrième manette est enfoncé. |



 

</dd> <dt>

<span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*
</dt> <dd>

Coordonnée z de la manette de jeu.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Manette](joysticks.md)
</dt> <dt>

[Messages de manette de jeu multimédia](multimedia-joystick-messages.md)
</dt> </dl>

 

 





