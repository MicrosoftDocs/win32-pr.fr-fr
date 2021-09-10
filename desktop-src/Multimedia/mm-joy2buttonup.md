---
title: Message MM_JOY2BUTTONUP (mmsystem. h)
description: Le \_ message JOY2BUTTONUP mm notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID2 qu’un bouton a été relâché.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- message MM_JOY2BUTTONUP Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367532"
---
# <a name="mm_joy2buttonup-message"></a>MM \_ message JOY2BUTTONUP

Le **message \_ JOY2BUTTONUP mm** notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID2 qu’un bouton a été relâché.


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

**fwButtons** 
</dt> <dd>

Identifie le bouton qui a changé d’État et les boutons qui sont enfoncés. Les valeurs possibles sont les suivantes :



| Valeur                                                                                                                                                            | Signification                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <dt>**JOIE \_ BUTTON1CHG**</dt> </dl> | Le premier bouton de la manette de jeu a changé d’État.<br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <dt>**JOIE \_ BUTTON2CHG**</dt> </dl> | Le deuxième bouton de la manette de jeu a changé d’État.<br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <dt>**JOIE \_ BUTTON3CHG**</dt> </dl> | Le bouton de la troisième manette de jeu a changé d’État.<br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <dt>**JOIE \_ BUTTON4CHG**</dt> </dl> | Le bouton de la quatrième manette de la manette a changé d’État.<br/> |



 

et un ou plusieurs des éléments suivants :



| Valeur                                                                                                                                                   | Signification                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <dt>**JOIE, \_ Button1**</dt> </dl> | Le premier bouton de la manette de jeu est enfoncé.<br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <dt>**BONHEUR \_ button2**</dt> </dl> | Le second bouton de la manette de jeu est enfoncé.<br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <dt>**BONHEUR \_ BUTTON3**</dt> </dl> | Le bouton de la manette de jeu est enfoncé.<br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <dt>**JOIE \_ BUTTON4**</dt> </dl> | Le bouton de la quatrième manette est enfoncé.<br/> |



 

</dd> <dt>

**xPos** 
</dt> <dd>

Coordonnées x de la manette de jeu par rapport au coin supérieur gauche de la zone cliente.

</dd> <dt>

**PosY** 
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

 

 





