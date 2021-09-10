---
title: Capture de l’entrée de manette
description: Capture de l’entrée de manette
ms.assetid: 1214fe5a-5a6a-4c6c-9b77-94eeb73f60da
keywords:
- joysticks, capture d’entrée
- capture de l’entrée de manette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23fd3717ad09fd2e52f1a815f7d13b91963a13e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367548"
---
# <a name="capturing-joystick-input"></a>Capture de l’entrée de manette

La plupart du code contrôlant la manette de jeu se trouve dans la fonction de fenêtre principale. Dans la partie suivante du gestionnaire de messages, l’application appelle [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) pour capturer l’entrée de la manette de jeu JOYSTICKID1.


```C++
case WM_CREATE: 
    if(joySetCapture(hWnd, JOYSTICKID1, NULL, FALSE)) 
    { 
        MessageBeep(MB_ICONEXCLAMATION); 
        MessageBox(hWnd, "Couldn't capture the joystick.", NULL, 
            MB_OK | MB_ICONEXCLAMATION); 
        PostMessage(hWnd,WM_CLOSE,0,0L); 
    } 
    break; 
 
```



 

 