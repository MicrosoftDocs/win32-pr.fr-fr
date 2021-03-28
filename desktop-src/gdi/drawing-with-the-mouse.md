---
description: Vous pouvez autoriser l’utilisateur à dessiner des lignes avec la souris en faisant glisser la procédure de la fenêtre pendant le traitement du \_ message WM MOUSEMOVE.
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: Dessin avec la souris
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ad38e7ef8af5c39918bac7231aea4dde285caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034226"
---
# <a name="drawing-with-the-mouse"></a>Dessin avec la souris

Vous pouvez autoriser l’utilisateur à dessiner des lignes avec la souris en faisant glisser la procédure de la fenêtre pendant le traitement du message [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) . Le système envoie le message **WM \_ MOUSEMOVE** à la procédure de fenêtre chaque fois que l’utilisateur déplace le curseur dans la fenêtre. Pour dessiner des lignes, la procédure de fenêtre peut récupérer un contexte de périphérique d’affichage et dessiner une ligne dans la fenêtre entre les positions actuelles et précédentes du curseur.

Dans l’exemple suivant, la procédure de fenêtre prépare le dessin lorsque l’utilisateur appuie sur le bouton gauche de la souris (en envoyant le message [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) ). Lorsque l’utilisateur déplace le curseur dans la fenêtre, la procédure de fenêtre reçoit une série de messages [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) . Pour chaque message, la procédure de fenêtre dessine une ligne reliant la position précédente et la position actuelle. Pour dessiner la ligne, la procédure utilise [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) pour récupérer un contexte de périphérique d’affichage. Ensuite, dès que le dessin est terminé et avant de retourner à partir du message, la procédure utilise la fonction [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) pour libérer le contexte de périphérique d’affichage. Dès que l’utilisateur relâche le bouton de la souris, la procédure de fenêtre efface l’indicateur et le dessin s’arrête (ce qui envoie le message [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) ).


```C++
BOOL fDraw = FALSE; 
POINT ptPrevious; 
 
  . 
  . 
  . 
 
case WM_LBUTTONDOWN: 
    fDraw = TRUE; 
    ptPrevious.x = LOWORD(lParam); 
    ptPrevious.y = HIWORD(lParam); 
    return 0L; 
 
case WM_LBUTTONUP: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, LOWORD(lParam), HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    fDraw = FALSE; 
    return 0L; 
 
case WM_MOUSEMOVE: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, ptPrevious.x = LOWORD(lParam), 
          ptPrevious.y = HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    return 0L; 
```



Une application qui active le dessin, comme dans cet exemple, enregistre généralement les points ou les lignes afin que les lignes puissent être redessinées chaque fois que la fenêtre est mise à jour. Les applications de dessin utilisent souvent un contexte de périphérique de mémoire et une image bitmap associée pour stocker des lignes qui ont été dessinées à l’aide d’une souris.

 

 
