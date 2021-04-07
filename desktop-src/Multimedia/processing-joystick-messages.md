---
title: Traitement des messages de manette de jeu
description: Traitement des messages de manette de jeu
ms.assetid: d21a9d49-1fc0-4899-9083-87c3cf4e0e62
keywords:
- manettes, messages
- Message MM_JOY1MOVE
- Message MM_JOY1BUTTONDOWN
- Message MM_JOY1BUTTONUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f2337d392c0104dcb49839b19c5fb615481ee2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029012"
---
# <a name="processing-joystick-messages"></a>Traitement des messages de manette de jeu

L’exemple suivant montre comment une application peut répondre aux mouvements de la manette de jeu et aux modifications apportées aux États du bouton. Lorsque la manette de jeu change de position, l’application déplace le curseur et, si l’un des deux boutons est enfoncé, dessine un trou à puces sur le bureau. Quand vous appuyez sur un bouton de manette de jeu, l’application dessine un trou sur le bureau et émet un son en continu jusqu’à ce qu’un bouton soit relâché. Les messages à surveiller sont [**mm \_ JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1BUTTONDOWN**](mm-joy1buttondown.md)et [**mm \_ JOY1BUTTONUP**](mm-joy1buttonup.md).


```C++
case MM_JOY1MOVE :                     // changed position 
    if((UINT) wParam & (JOY_BUTTON1 | JOY_BUTTON2)) 
        DrawFire(hWnd); 
    DrawSight(lParam);                 // calculates new cursor position 
    break; 
case MM_JOY1BUTTONDOWN :               // button is down 
    if((UINT) wParam & JOY_BUTTON1) 
    { 
        PlaySound(lpButton1, SND_LOOP | SND_ASYNC | SND_MEMORY); 
        DrawFire(hWnd); 
    } 
    else if((UINT) wParam & JOY_BUTTON2) 
    { 
        PlaySound(lpButton2, SND_ASYNC | SND_MEMORY |  SND_LOOP); 
        DrawFire(hWnd); 
    } 
    break; 
case MM_JOY1BUTTONUP :                 // button is up 
    sndPlaySound(NULL, 0);             // stops the sound 
    break; 

```



 

 




