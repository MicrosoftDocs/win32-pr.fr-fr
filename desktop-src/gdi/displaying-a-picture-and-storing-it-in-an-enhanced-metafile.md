---
description: Cette section contient un exemple illustrant la création d’une image et le processus de stockage des enregistrements correspondants dans un métafichier.
ms.assetid: 8be95fef-93dc-4c9c-a0d3-840918c00e43
title: Affichage d’une image et stockage dans un métafichier amélioré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8eee65f2f82a7b8ccdad86e99987df6a06a4f5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754436"
---
# <a name="displaying-a-picture-and-storing-it-in-an-enhanced-metafile"></a><span data-ttu-id="11f88-103">Affichage d’une image et stockage dans un métafichier amélioré</span><span class="sxs-lookup"><span data-stu-id="11f88-103">Displaying a Picture and Storing It in an Enhanced Metafile</span></span>

<span data-ttu-id="11f88-104">Cette section contient un exemple illustrant la création d’une image et le processus de stockage des enregistrements correspondants dans un métafichier.</span><span class="sxs-lookup"><span data-stu-id="11f88-104">This section contains an example demonstrating the creation of a picture and the process of storing the corresponding records in a metafile.</span></span> <span data-ttu-id="11f88-105">L’exemple dessine une image à l’écran ou la stocke dans un métafichier.</span><span class="sxs-lookup"><span data-stu-id="11f88-105">The example draws a picture to the display or stores it in a metafile.</span></span> <span data-ttu-id="11f88-106">Si un handle de contexte de périphérique d’affichage est donné, il dessine une image à l’écran à l’aide de différentes fonctions GDI.</span><span class="sxs-lookup"><span data-stu-id="11f88-106">If a display device context handle is given, it draws a picture to the screen using various GDI functions.</span></span> <span data-ttu-id="11f88-107">Si un contexte de périphérique de métafichier amélioré est donné, il stocke la même image dans le métafichier amélioré.</span><span class="sxs-lookup"><span data-stu-id="11f88-107">If an enhanced metafile device context is given, it stores the same picture in the enhanced metafile.</span></span>


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



 

 



