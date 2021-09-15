---
description: Cette section contient un exemple illustrant la création d’une image et le processus de stockage des enregistrements correspondants dans un métafichier.
ms.assetid: 8be95fef-93dc-4c9c-a0d3-840918c00e43
title: Affichage d’une image et stockage dans un métafichier amélioré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8eee65f2f82a7b8ccdad86e99987df6a06a4f5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531977"
---
# <a name="displaying-a-picture-and-storing-it-in-an-enhanced-metafile"></a>Affichage d’une image et stockage dans un métafichier amélioré

Cette section contient un exemple illustrant la création d’une image et le processus de stockage des enregistrements correspondants dans un métafichier. L’exemple dessine une image à l’écran ou la stocke dans un métafichier. Si un handle de contexte de périphérique d’affichage est donné, il dessine une image à l’écran à l’aide de différentes fonctions GDI. Si un contexte de périphérique de métafichier amélioré est donné, il stocke la même image dans le métafichier amélioré.


```C++
void DrawOrStore(HWND hwnd, HDC hdcMeta, HDC hdcDisplay) 
{ 
 
RECT rect; 
HDC hDC; 
int fnMapModeOld; 
HBRUSH hbrOld; 
 
// Draw it to the display DC or store it in the metafile device context.  
 
if (hdcMeta) 
    hDC = hdcMeta; 
else 
    hDC = hdcDisplay; 
 
// Set the mapping mode in the device context.  
 
fnMapModeOld = SetMapMode(hDC, MM_LOENGLISH); 
 
// Find the midpoint of the client area.  
 
GetClientRect(hwnd, (LPRECT)&rect); 
DPtoLP(hDC, (LPPOINT)&rect, 2); 
 
// Select a gray brush.  
 
hbrOld = SelectObject(hDC, GetStockObject(GRAY_BRUSH)); 
 
// Draw a circle with a one inch radius.  
 
Ellipse(hDC, (rect.right/2 - 100), (rect.bottom/2 + 100), 
       (rect.right/2 + 100), (rect.bottom/2 - 100)); 
 
// Perform additional drawing here.  
 
 
 
// Set the device context back to its original state.  
 
SetMapMode(hDC, fnMapModeOld); 
SelectObject(hDC, hbrOld); 
} 
```



 

 



