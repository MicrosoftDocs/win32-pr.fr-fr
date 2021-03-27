---
description: Vous pouvez utiliser les fonctions de ligne pour dessiner des marqueurs.
ms.assetid: 69114875-f3e0-45e9-8e87-1f4e9de08db1
title: Marqueurs de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b725e3a266e296950394a9bb9b2b76a17cb25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754429"
---
# <a name="drawing-markers"></a><span data-ttu-id="e83fc-103">Marqueurs de dessin</span><span class="sxs-lookup"><span data-stu-id="e83fc-103">Drawing Markers</span></span>

<span data-ttu-id="e83fc-104">Vous pouvez utiliser les fonctions de ligne pour dessiner des marqueurs.</span><span class="sxs-lookup"><span data-stu-id="e83fc-104">You can use the line functions to draw markers.</span></span> <span data-ttu-id="e83fc-105">Un marqueur est un symbole centré sur un point.</span><span class="sxs-lookup"><span data-stu-id="e83fc-105">A marker is a symbol centered over a point.</span></span> <span data-ttu-id="e83fc-106">Les applications de dessin utilisent des marqueurs pour désigner des points de départ, des points de fin et des points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="e83fc-106">Drawing applications use markers to designate starting points, ending points, and control points.</span></span> <span data-ttu-id="e83fc-107">Les applications de feuille de calcul utilisent des marqueurs pour désigner des points d’intérêt sur un graphique ou un graphique.</span><span class="sxs-lookup"><span data-stu-id="e83fc-107">Spreadsheet applications use markers to designate points of interest on a chart or graph.</span></span>

<span data-ttu-id="e83fc-108">Dans l’exemple de code suivant, la fonction de marqueur définie par l’application crée un marqueur à l’aide des fonctions [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) et [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) .</span><span class="sxs-lookup"><span data-stu-id="e83fc-108">In the following code sample, the application-defined Marker function creates a marker by using the [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) and [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) functions.</span></span> <span data-ttu-id="e83fc-109">Ces fonctions dessinent deux lignes d’intersection, d’une longueur de 20 pixels, centrées sur les coordonnées du curseur.</span><span class="sxs-lookup"><span data-stu-id="e83fc-109">These functions draw two intersecting lines, 20 pixels in length, centered over the cursor coordinates.</span></span>


```C++
void Marker(LONG x, LONG y, HWND hwnd) 
{ 
    HDC hdc; 
 
    hdc = GetDC(hwnd); 
        MoveToEx(hdc, (int) x - 10, (int) y, (LPPOINT) NULL); 
        LineTo(hdc, (int) x + 10, (int) y); 
        MoveToEx(hdc, (int) x, (int) y - 10, (LPPOINT) NULL); 
        LineTo(hdc, (int) x, (int) y + 10); 

    ReleaseDC(hwnd, hdc); 
} 
```



<span data-ttu-id="e83fc-110">Le système stocke les coordonnées du curseur dans le paramètre *lParam* du message [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) quand l’utilisateur appuie sur le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="e83fc-110">The system stores the coordinates of the cursor in the *lParam* parameter of the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message when the user presses the left mouse button.</span></span> <span data-ttu-id="e83fc-111">Le code suivant montre comment une application obtient ces coordonnées, détermine si elles se trouvent dans sa zone cliente et les transmet à la fonction de marqueur pour dessiner le marqueur.</span><span class="sxs-lookup"><span data-stu-id="e83fc-111">The following code demonstrates how an application gets these coordinates, determines whether they lie within its client area, and passes them to the Marker function to draw the marker.</span></span>


```C++
// Line- and arc-drawing variables  
 
static BOOL bCollectPoints; 
static POINT ptMouseDown[32]; 
static int index; 
POINTS ptTmp; 
RECT rc; 
 
    case WM_LBUTTONDOWN: 
 
 
        if (bCollectPoints && index < 32)
        { 
            // Create the region from the client area.  
 
            GetClientRect(hwnd, &rc); 
            hrgn = CreateRectRgn(rc.left, rc.top, 
                rc.right, rc.bottom); 
 
            ptTmp = MAKEPOINTS((POINTS FAR *) lParam); 
            ptMouseDown[index].x = (LONG) ptTmp.x; 
            ptMouseDown[index].y = (LONG) ptTmp.y; 
 
            // Test for a hit in the client rectangle.  
 
            if (PtInRegion(hrgn, ptMouseDown[index].x, 
                    ptMouseDown[index].y)) 
            { 
                // If a hit occurs, record the mouse coords.  
 
                Marker(ptMouseDown[index].x, ptMouseDown[index].y, 
                    hwnd); 
                index++; 
            } 
        } 
        break; 
```



 

 
