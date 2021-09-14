---
title: Message MM_JOY2BUTTONDOWN (mmsystem. h)
description: Le \_ message JOY2BUTTONDOWN mm notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID2 qu’un bouton a été enfoncé.
ms.assetid: b4cd48ea-91ad-48e9-b0ae-58d8ee124171
keywords:
- message MM_JOY2BUTTONDOWN Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f155fcdc21247e01fd5d730f3f7d4daaba705e65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233802"
---
# <a name="mm_joy2buttondown-message"></a>MM \_ message JOY2BUTTONDOWN

Le **message \_ JOY2BUTTONDOWN mm** notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID2 qu’un bouton a été enfoncé.


```C++
MM_JOY2BUTTONDOWN 
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

Coordonnées x de la manette de jeu par rapport au coin supérieur gauche de la zone cliente.

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

 

 





