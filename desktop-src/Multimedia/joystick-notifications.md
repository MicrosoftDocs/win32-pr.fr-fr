---
title: Notifications de manette de jeu
description: Notifications de manette de jeu
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- manettes de jeu, notifications
- manettes, messages
- joysticks capturés
- joysticks débranchés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2791f8da14107d50afe90d8efbdbfe79acba3093
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195223"
---
# <a name="joystick-notifications"></a>Notifications de manette de jeu

Vous pouvez capturer des messages de manette de jeu directs à envoyer à une fonction à l’aide de la fonction [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) . Une seule application à la fois peut capturer des messages à partir d’une manette de jeu, mais vous pouvez interroger la manette de jeu à partir d’une autre application à l’aide de la fonction [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) ou [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .

> [!Note]  
> Un message de manette de jeu peut ne pas parvenir à atteindre l’application qui a capturé la manette de jeu si une deuxième application utilise **joyGetPos** ou **joyGetPosEx** pour interroger la manette à peu près au même moment que le message est envoyé. Dans ce cas, la deuxième application peut intercepter le message.

 

Si vous souhaitez capturer des messages à partir de deux manettes associées au système, utilisez [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) à deux reprises, une fois pour chaque manette de jeu. Votre fenêtre reçoit des messages distincts et distincts pour chaque appareil.

Vous pouvez libérer une manette capturée à l’aide de la fonction [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) . Si une application ne libère pas la manette de jeu avant de se terminer, la manette de jeu est automatiquement libérée peu après la destruction de la fenêtre de capture.

Vous ne pouvez pas capturer une manette débranchée. La fonction **joySetCapture** retourne JOYERR \_ débranché si l’appareil spécifié est débranché.

 

 