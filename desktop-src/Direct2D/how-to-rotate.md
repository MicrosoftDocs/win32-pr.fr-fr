---
title: Comment faire pivoter un objet
description: Montre comment faire pivoter un objet.
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cd900a78ba4d81919df91b85fd97723172eba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113090"
---
# <a name="how-to-rotate-an-object"></a>Comment faire pivoter un objet

Cette rubrique explique comment faire pivoter un objet à propos d’un point spécifié. Pour faire pivoter un objet, appelez la méthode [**Matrix3x2F :: rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) . Cette méthode prend deux paramètres, l’angle spécifié et le point central. L’angle est un angle de rotation dans le sens des aiguilles d’une montre, en degrés, et le point central est le point sur lequel l’objet pivote. Le point central est exprimé dans le système de coordonnées de l’objet transformé.

Par exemple, le code suivant fait pivoter un carré dans le sens des aiguilles d’une montre à 45 degrés autour du centre du carré.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



L’illustration suivante montre l’effet de l’application de la transformation de rotation précédente au carré. Le carré d’origine est un contour en pointillés, et le carré pivoté est un contour Uni.

![illustration d’un carré pivoté dans le sens des aiguilles d’une montre à 45 degrés à propos du centre du carré d’origine](images/rotate-ovw.png)

L’illustration suivante montre l’effet de la rotation par le même angle sur un point central différent. Notez que les objets pivotés se trouvent à des positions différentes par rapport à l’original. Le carré à gauche est le résultat d’une rotation autour du centre du carré d’origine, tandis que le carré droit est le résultat d’une rotation autour de l’angle supérieur gauche du carré d’origine.

![illustration d’un carré pivoté dans le sens des aiguilles d’une montre à 45 degrés à propos d’un point central différent](images/translate-rotationcompare.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> <dt>

[Vue d’ensemble des transformations Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 