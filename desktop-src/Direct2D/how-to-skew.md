---
title: Comment incliner un objet
description: Montre comment incliner un objet.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691062e64d4255b1e2f7711b5ff700d72fd90063
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113086"
---
# <a name="how-to-skew-an-object"></a>Comment incliner un objet

Pour incliner (ou cisailler) un objet signifie qu’il doit déformer un objet d’un angle spécifié par rapport à l’axe des x, à l’axe des y ou aux deux. Par exemple, lorsque vous inclinez un carré, il devient un parallélogramme.

La méthode [**Matrix3x2F :: skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) utilise 3 paramètres :

-   *AngleX*: angle d’inclinaison de l’axe x, mesuré en degrés dans le sens inverse des aiguilles d’une position à partir de l’axe y.
-   *AngleY*: angle d’inclinaison de l’axe y, mesuré en degrés dans le sens des aiguilles d’une montre à partir de l’axe x.
-   *centerPoint*: point sur lequel l’inclinaison est exécutée.

Pour prédire l’effet d’une transformation d’inclinaison, prenez en compte que *AngleX* est l’angle d’inclinaison mesuré en degrés dans le sens inverse des aiguilles d’une position à partir de l’axe y. Par exemple, si *AngleX* a la valeur 30, l’objet passe à 30 degrés dans le sens inverse des aiguilles d’une montre sur l’axe y du *centerPoint*. L’illustration suivante montre un décalage carré horizontal de 30 degrés par-dessus le coin supérieur gauche du carré.

![illustration d’un carré incliné de 30 degrés dans le sens inverse des aiguilles d’une montre à partir de l’axe y](images/skewx.png)

De même, *AngleY* est un angle d’inclinaison mesuré en degrés dans le sens des aiguilles d’une montre à partir de l’axe x. Par exemple, si *AngleY* est défini sur 30, l’objet passe à 30 degrés dans le sens horaire le long de l’axe x à propos du *centerPoint*. L’illustration suivante montre un décalage carré vertical de 30 degrés par-dessus le coin supérieur gauche du carré.

![illustration d’un carré incliné 30 degrés dans le sens des aiguilles d’une montre à partir de l’axe x](images/skewy.png)

Si vous définissez à la fois *AngleX* et *AngleY* sur 30 degrés, et *centerPoint* sur l’angle supérieur gauche du carré, vous verrez le carré incliné suivant (entouré d’une forme unie). Notez que le carré incliné est incliné de 30 degrés dans le sens inverse des aiguilles d’une montre à partir de l’axe y et de 30 degrés dans le sens des aiguilles d’une montre à partir de l’axe x.

![illustration d’un carré incliné de 30 degrés dans le sens inverse des aiguilles d’une montre à partir de l’axe y et de 30 degrés dans le sens horaire à partir de l’axe x](images/skewxy.png)

L’exemple de code suivant incline le carré de 45 degrés horizontalement autour de l’angle supérieur gauche du carré.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 301.5f, 186.0f, 361.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the skew transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Skew(
            45.0f,
            0.0f,
            D2D1::Point2F(126.0f, 301.5f))
        );

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



L’illustration suivante montre l’effet de l’application de la transformation d’inclinaison au carré, où le carré d’origine est un contour en pointillés et l’objet incliné (parallélogramme) est un contour solide. Notez que l’angle d’inclinaison est de 45 degrés dans le sens inverse des aiguilles d’une position à partir de l’axe y.

![illustration d’un carré incliné de 45 degrés dans le sens inverse des aiguilles d’une montre à partir de l’axe y](images/skew-ovw.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des transformations Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 