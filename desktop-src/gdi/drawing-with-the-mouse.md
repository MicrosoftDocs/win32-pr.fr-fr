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
# <a name="drawing-with-the-mouse"></a><span data-ttu-id="39b50-103">Dessin avec la souris</span><span class="sxs-lookup"><span data-stu-id="39b50-103">Drawing with the Mouse</span></span>

<span data-ttu-id="39b50-104">Vous pouvez autoriser l’utilisateur à dessiner des lignes avec la souris en faisant glisser la procédure de la fenêtre pendant le traitement du message [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) .</span><span class="sxs-lookup"><span data-stu-id="39b50-104">You can permit the user to draw lines with the mouse by having your window procedure draw while processing the [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) message.</span></span> <span data-ttu-id="39b50-105">Le système envoie le message **WM \_ MOUSEMOVE** à la procédure de fenêtre chaque fois que l’utilisateur déplace le curseur dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="39b50-105">The system sends the **WM\_MOUSEMOVE** message to the window procedure whenever the user moves the cursor within the window.</span></span> <span data-ttu-id="39b50-106">Pour dessiner des lignes, la procédure de fenêtre peut récupérer un contexte de périphérique d’affichage et dessiner une ligne dans la fenêtre entre les positions actuelles et précédentes du curseur.</span><span class="sxs-lookup"><span data-stu-id="39b50-106">To draw lines, the window procedure can retrieve a display device context and draw a line in the window between the current and previous cursor positions.</span></span>

<span data-ttu-id="39b50-107">Dans l’exemple suivant, la procédure de fenêtre prépare le dessin lorsque l’utilisateur appuie sur le bouton gauche de la souris (en envoyant le message [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) ).</span><span class="sxs-lookup"><span data-stu-id="39b50-107">In the following example, the window procedure prepares for drawing when the user presses and holds the left mouse button (sending the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message).</span></span> <span data-ttu-id="39b50-108">Lorsque l’utilisateur déplace le curseur dans la fenêtre, la procédure de fenêtre reçoit une série de messages [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) .</span><span class="sxs-lookup"><span data-stu-id="39b50-108">As the user moves the cursor within the window, the window procedure receives a series of [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) messages.</span></span> <span data-ttu-id="39b50-109">Pour chaque message, la procédure de fenêtre dessine une ligne reliant la position précédente et la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="39b50-109">For each message, the window procedure draws a line connecting the previous position and the current position.</span></span> <span data-ttu-id="39b50-110">Pour dessiner la ligne, la procédure utilise [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) pour récupérer un contexte de périphérique d’affichage. Ensuite, dès que le dessin est terminé et avant de retourner à partir du message, la procédure utilise la fonction [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) pour libérer le contexte de périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="39b50-110">To draw the line, the procedure uses [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) to retrieve a display device context; then, as soon as drawing is complete and before returning from the message, the procedure uses the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function to release the display device context.</span></span> <span data-ttu-id="39b50-111">Dès que l’utilisateur relâche le bouton de la souris, la procédure de fenêtre efface l’indicateur et le dessin s’arrête (ce qui envoie le message [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) ).</span><span class="sxs-lookup"><span data-stu-id="39b50-111">As soon as the user releases the mouse button, the window procedure clears the flag, and the drawing stops (which sends the [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) message).</span></span>


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



<span data-ttu-id="39b50-112">Une application qui active le dessin, comme dans cet exemple, enregistre généralement les points ou les lignes afin que les lignes puissent être redessinées chaque fois que la fenêtre est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="39b50-112">An application that enables drawing, as in this example, typically records either the points or lines so that the lines can be redrawn whenever the window is updated.</span></span> <span data-ttu-id="39b50-113">Les applications de dessin utilisent souvent un contexte de périphérique de mémoire et une image bitmap associée pour stocker des lignes qui ont été dessinées à l’aide d’une souris.</span><span class="sxs-lookup"><span data-stu-id="39b50-113">Drawing applications often use a memory device context and an associated bitmap to store lines that were drawn by using a mouse.</span></span>

 

 
