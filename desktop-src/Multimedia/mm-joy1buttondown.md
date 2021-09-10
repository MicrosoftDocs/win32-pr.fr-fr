---
title: Message MM_JOY1BUTTONDOWN (mmsystem. h)
description: Le \_ message JOY1BUTTONDOWN mm notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID1 qu’un bouton a été enfoncé.
ms.assetid: 764f4bb4-134d-46b8-badb-3fb06af31e13
keywords:
- message MM_JOY1BUTTONDOWN Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cefb70e5dd47fc14b39dcdeb59043b6827e7b89b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364571"
---
# <a name="mm_joy1buttondown-message"></a>MM \_ message JOY1BUTTONDOWN

Le **message \_ JOY1BUTTONDOWN mm** notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID1 qu’un bouton a été enfoncé.


```C++
MM_JOY1BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifie le bouton qui a changé d’État et les boutons qui sont enfoncés. Les valeurs possibles sont les suivantes :



| Condition requise | Valeur |
|-----------------|-------------------------------------------|
| JOIE \_ BUTTON1CHG | Le premier bouton de la manette de jeu a changé d’État.  |
| JOIE \_ BUTTON2CHG | Le deuxième bouton de la manette de jeu a changé d’État. |
| JOIE \_ BUTTON3CHG | Le bouton de la troisième manette de jeu a changé d’État.  |
| JOIE \_ BUTTON4CHG | Le bouton de la quatrième manette de la manette a changé d’État. |



 

et un ou plusieurs des éléments suivants :



| Condition requise | Valeur |
|--------------|------------------------------------|
| JOIE, \_ Button1 | Le premier bouton de la manette de jeu est enfoncé.  |
| BONHEUR \_ button2 | Le second bouton de la manette de jeu est enfoncé. |
| BONHEUR \_ BUTTON3 | Le bouton de la manette de jeu est enfoncé.  |
| JOIE \_ BUTTON4 | Le bouton de la quatrième manette est enfoncé. |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Coordonnée x de la manette de jeu par rapport au coin supérieur gauche de la zone cliente.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*PosY*
</dt> <dd>

Coordonnée y de la manette de jeu par rapport au coin supérieur gauche de la zone cliente.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Manette](joysticks.md)
</dt> <dt>

[Messages de manette de jeu multimédia](multimedia-joystick-messages.md)
</dt> </dl>

 

 





