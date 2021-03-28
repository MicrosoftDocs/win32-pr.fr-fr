---
description: Pour répondre à un \_ message de peinture WM, utilisez un code similaire à celui-ci.
ms.assetid: 682d9bc6-8d74-48c4-80fb-bae73d409a6b
title: Peinture sur un contrôleur de périphérique qui s’étend sur plusieurs affichages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5b1b85c8aab20b7ef2415c1d67188ecab7728c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528311"
---
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a>Peinture sur un contrôleur de périphérique qui s’étend sur plusieurs affichages

Pour répondre à un message de **\_ peinture WM** , utilisez un code similaire à celui-ci.


```C++
case WM_PAINT:
hdc = BeginPaint(hwnd, &ps);
EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
EndPaint(hwnd, &ps);
 
```



Pour peindre la moitié supérieure d’une fenêtre, utilisez un code similaire à ce qui suit.


```C++
GetClient Rect(hwnd, &rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
```



Pour peindre l’intégralité de l’écran virtuel de façon optimale pour chaque moniteur, utilisez un code similaire à celui-ci.


```C++
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
```



 

 



