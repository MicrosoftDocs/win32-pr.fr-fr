---
description: Pour dessiner un rectangle ombré, définissez un tableau de TRIVERTEX avec deux éléments et une seule structure de Rect de dégradé \_ . L’exemple de code suivant montre comment dessiner un rectangle ombré à l’aide de la fonction GradientFill avec le mode rectangle de \_ remplissage dégradé \_ défini.
ms.assetid: a4277e22-03f8-470f-87e9-5aeab258b6d2
title: Dessin d’un rectangle ombré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665e76c730ada1bd8efc9967fd10e550f0aa2e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528360"
---
# <a name="drawing-a-shaded-rectangle"></a>Dessin d’un rectangle ombré

Pour dessiner un rectangle ombré, définissez un tableau de [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) avec deux éléments et une seule structure de [**\_ Rect de dégradé**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect) . L’exemple de code suivant montre comment dessiner un rectangle ombré à l’aide de la fonction [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) avec le mode rectangle de \_ remplissage dégradé \_ défini.


```C++
// Create an array of TRIVERTEX structures that describe 
// positional and color values for each vertex. For a rectangle, 
// only two vertices need to be defined: upper-left and lower-right. 
TRIVERTEX vertex[2] ;
vertex[0].x     = 0;
vertex[0].y     = 0;
vertex[0].Red   = 0x0000;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x8000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 300;
vertex[1].y     = 80; 
vertex[1].Red   = 0x0000;
vertex[1].Green = 0xd000;
vertex[1].Blue  = 0xd000;
vertex[1].Alpha = 0x0000;

// Create a GRADIENT_RECT structure that 
// references the TRIVERTEX vertices. 
GRADIENT_RECT gRect;
gRect.UpperLeft  = 0;
gRect.LowerRight = 1;

// Draw a shaded rectangle. 
GradientFill(hdc, vertex, 2, &gRect, 1, GRADIENT_FILL_RECT_H);
```



L’illustration suivante montre la sortie de dessin de l’exemple de code précédent.

![Illustration montrant un rectangle avec un remplissage dégradé de foncé sur le côté gauche jusqu’à la lumière située à droite](images/gradientfillrectangle.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des bitmaps](bitmaps.md)
</dt> <dt>

[Fonctions bitmap](bitmap-functions.md)
</dt> <dt>

[Dessin d’un triangle ombré](drawing-a-shaded-triangle.md)
</dt> <dt>

[**EMRGRADIENTFILL**](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[**\_rectangle dégradé**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)
</dt> <dt>

[**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



