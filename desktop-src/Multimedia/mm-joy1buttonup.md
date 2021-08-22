---
title: Message MM_JOY1BUTTONUP (mmsystem. h)
description: Le \_ message JOY1BUTTONUP mm notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID1 qu’un bouton a été relâché.
ms.assetid: 37f0f87a-4805-4cec-9c0c-9d6b36a3ff0d
keywords:
- message MM_JOY1BUTTONUP Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70c7b8dda57d91e595bd65223a2fd33ef904679e35a38aaacbaf263b525258f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065569"
---
# <a name="mm_joy1buttonup-message"></a>MM \_ message JOY1BUTTONUP

Le **message \_ JOY1BUTTONUP mm** notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID1 qu’un bouton a été relâché.


```C++
MM_JOY1BUTTONUP 
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

## <a name="requirements"></a>Configuration requise



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

 

 





