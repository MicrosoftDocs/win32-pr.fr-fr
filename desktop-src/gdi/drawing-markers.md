---
description: Vous pouvez utiliser les fonctions de ligne pour dessiner des marqueurs.
ms.assetid: 69114875-f3e0-45e9-8e87-1f4e9de08db1
title: Marqueurs de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5e05c651bf95aa48a8ef11fd0819523ee5da7652e27ecebaeff8ee9de4f1e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887117"
---
# <a name="drawing-markers"></a>Marqueurs de dessin

Vous pouvez utiliser les fonctions de ligne pour dessiner des marqueurs. Un marqueur est un symbole centré sur un point. Les applications de dessin utilisent des marqueurs pour désigner des points de départ, des points de fin et des points de contrôle. Les applications de feuille de calcul utilisent des marqueurs pour désigner des points d’intérêt sur un graphique ou un graphique.

Dans l’exemple de code suivant, la fonction de marqueur définie par l’application crée un marqueur à l’aide des fonctions [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) et [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) . Ces fonctions dessinent deux lignes d’intersection, d’une longueur de 20 pixels, centrées sur les coordonnées du curseur.


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



Le système stocke les coordonnées du curseur dans le paramètre *lParam* du message [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) quand l’utilisateur appuie sur le bouton gauche de la souris. Le code suivant montre comment une application obtient ces coordonnées, détermine si elles se trouvent dans sa zone cliente et les transmet à la fonction de marqueur pour dessiner le marqueur.


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



 

 
