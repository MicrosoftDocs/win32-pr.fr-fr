---
title: Obtention des fonctionnalités du pilote
description: Obtention des fonctionnalités du pilote
ms.assetid: 761886db-b2e5-449c-b526-6e992cc1b42f
keywords:
- manettes, pilotes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b9f4d54e80dc589a4c730ef891d8f0bd132e52
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367551"
---
# <a name="getting-the-driver-capabilities"></a>Obtention des fonctionnalités du pilote

L’exemple suivant utilise [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) et [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) pour déterminer si les services de la manette de jeu sont disponibles et si une manette de jeu est attachée à l’un des ports.


```C++
JOYINFO joyinfo; 
UINT wNumDevs, wDeviceID; 
BOOL bDev1Attached, bDev2Attached; 
 
    if((wNumDevs = joyGetNumDevs()) == 0) 
        return ERR_NODRIVER; 
    bDev1Attached = joyGetPos(JOYSTICKID1,&joyinfo) != JOYERR_UNPLUGGED; 
    bDev2Attached = wNumDevs == 2 && joyGetPos(JOYSTICKID2,&joyinfo) != 
        JOYERR_UNPLUGGED; 
    if(bDev1Attached || bDev2Attached)   // decide which joystick to use 
        wDeviceID = bDev1Attached ? JOYSTICKID1 : JOYSTICKID2; 
    else 
        return ERR_NODEVICE; 

```



 

 