---
title: Mise à l’échelle d’un objet
description: Montre comment mettre à l’échelle un objet.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d833ea44e4a38672729dd7647063e8ed9f8de3574d820a3db40d5a848064ef15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259143"
---
# <a name="how-to-scale-an-object"></a>Mise à l’échelle d’un objet

Cette rubrique explique comment mettre à l’échelle un objet à l’aide de la classe [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) . La mise à l’échelle d’un objet signifie que l’objet est plus grand ou plus petit. Vous pouvez appeler l’une des deux méthodes suivantes pour mettre à l’échelle un objet.

-   **Matrix3x2F :: Scale (D2D1 \_ taille \_ F SCALEFACTOR, d2d1 \_ point \_ 2F Centerpoint)**
-   **Matrix3x2F :: Scale (float ScaleX, float ScaleY, D2D1 \_ point \_ 2F Centerpoint)**

La première méthode stocke *ScaleX* et *ScaleY* en tant que paire ordonnée de valeurs à virgule flottante dans la structure [**d2d1 \_ size \_ F**](/windows/desktop/Direct2D/d2d1-size-f) . La deuxième méthode définit *ScaleX* et *ScaleY* en tant que paramètres individuels.

Quelle que soit la méthode utilisée, vous devez spécifier des facteurs *ScaleX* et *ScaleY* . La valeur *ScaleX* est le facteur d’échelle sur l’axe x. Par exemple, une valeur *ScaleX* de 1,5 étire l’objet à 150% le long de l’axe x. De même, la valeur *ScaleY* est le facteur d’échelle sur l’axe y. Par exemple, une valeur *ScaleY* de 0,5 réduit la hauteur de l’objet de 50% le long de l’axe y.

Pour spécifier un point comme centre de l’opération de mise à l’échelle, utilisez le paramètre *Centerpoint* . Par défaut, un objet est centré sur son origine (0, 0).

L’exemple de code suivant crée une transformation d’échelle pour augmenter la taille d’un carré à 130% de sa taille d’origine. Le *Centerpoint* est défini comme étant l’angle supérieur gauche du carré d’origine.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 80.5f, 498.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the scale transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Scale(
            D2D1::Size(1.3f, 1.3f),
            D2D1::Point2F(438.0f, 80.5f))
        );

    // Paint the rectangle's interior.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



L’illustration suivante montre l’effet de l’application de la transformation d’échelle au carré. Le carré d’origine est un contour en pointillés et le carré mis à l’échelle est un contour plein.

![illustration du redimensionnement du carré à 130% de sa taille d’origine](images/scale-ovw.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des transformations Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 