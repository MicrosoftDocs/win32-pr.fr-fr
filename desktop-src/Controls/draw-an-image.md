---
title: Comment dessiner une image
description: Cette rubrique montre comment utiliser la fonction ImageList \_ Draw pour dessiner une image.
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac13eef2eb5bc55866ac2fd930db5494f2683dd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941500"
---
# <a name="how-to-draw-an-image"></a>Comment dessiner une image

Cette rubrique montre comment utiliser la fonction [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) pour dessiner une image.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions


Pour dessiner une image, vous utilisez la fonction [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) . Vous spécifiez le handle d’une liste d’images, l’index de l’image à dessiner, le handle vers le contexte de périphérique de destination, un emplacement dans le contexte de périphérique et un ou plusieurs styles de dessin.

La fonction définie par l’utilisateur dans l’exemple de code C++ suivant utilise la fonction de [**\_ dessin ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) pour dessiner une image et enregistre les coordonnées clientes du rectangle englobant de l’image. Une fonction suivante utilise le rectangle englobant pour déterminer si l’utilisateur a cliqué sur l’image.



```C++
// DrawTheImage - draws an image transparently and saves 
// the bounding rectangle of the drawn image.
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which to draw the image. 
// himl - handle to the image list that contains the image. 
// cx and cy - client coordinates for the upper-left corner of the image. 
// 
// Global variables and constants 
//     g_nImage - index of the image to draw. 
//     g_rcImage - bounding rectangle of the image. 
//     CX_IMAGE and CY_IMAGE - width and height of the image. 
extern int g_nImage; 
extern RECT g_rcImage; 
 
#define CX_IMAGE 32 
#define CY_IMAGE 32 
 
BOOL DrawTheImage(HWND hwnd, HIMAGELIST himl, int cx, int cy) 
{ 
    HDC hdc; 
 
    if ((hdc = GetDC(hwnd)) == NULL) 
        return FALSE; 
    if (!ImageList_Draw(himl, g_nImage, hdc, cx, cy, ILD_TRANSPARENT)) 
        return FALSE; 
    ReleaseDC(hwnd, hdc); 
 
    SetRect(&g_rcImage, cx, cy, CX_IMAGE + cx, CY_IMAGE + cy); 
 
    return TRUE; 
} 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur les listes d’images](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[À propos des listes d’images](image-lists.md)
</dt> <dt>

[Utilisation de listes d’images](using-image-lists.md)
</dt> </dl>

 

 




