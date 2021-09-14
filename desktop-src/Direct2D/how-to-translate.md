---
title: Comment traduire un objet
description: Montre comment traduire un objet.
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113081"
---
# <a name="how-to-translate-an-object"></a>Comment traduire un objet

La conversion d’un objet 2D consiste à déplacer l’objet le long de l’axe x, de l’axe y, ou les deux. Vous pouvez appeler l’une des deux méthodes suivantes pour créer une transformation de traduction.

-   [**Translation (taille \_ d2d1 \_ F)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): prend une paire ordonnée qui définit la distance de translation le long de l’axe x et de l’axe y.
-   [**Translation (float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): prend la distance pour effectuer la translation le long de l’axe x et la distance pour la translation le long de l’axe y.

Le code suivant crée une matrice de transformation de translation qui déplace le carré de 20 unités vers la droite le long de l’axe x et de 10 unités vers le bas le long de l’axe y.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 80.5f, 186.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the translation transform to the render target.
    m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(20, 10));

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



L’illustration suivante montre l’effet de l’application de la transformation de translation au carré, où le carré d’origine est un contour en pointillés et le carré traduit est un contour Uni.

![illustration d’un carré déplacé de 20 unités vers la droite le long de l’axe x et de 10 unités vers le côté de l’axe y](images/translation-ovw.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> <dt>

[Vue d’ensemble des transformations Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 