---
title: Comment dessiner une image
description: Cette rubrique montre comment utiliser la fonction ImageList \_ Draw pour dessiner une image.
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7b42e97ad9b7cab8693431654dc31b473267414f31ae5811f4f66a6663ce8e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878329"
---
# <a name="how-to-draw-an-image"></a>Comment dessiner une image

Cette rubrique montre comment utiliser la fonction [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) pour dessiner une image.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

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

 

 




