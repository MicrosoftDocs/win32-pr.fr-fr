---
title: Comment appliquer plusieurs transformations à un objet
description: Montre comment appliquer plusieurs transformations à un objet.
ms.assetid: a3875072-bb73-4698-944e-102ab5539d80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e031a46545c59513767ed4d260be9dc677b3fb77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113161"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a>Comment appliquer plusieurs transformations à un objet

Pour effectuer plusieurs transformations sur un objet, vous pouvez combiner plusieurs transformations en une seule. Autrement dit, en prenant la sortie de chaque matrice de transformation et en l’utilisant comme entrée pour la suivante, en obtenant les effets cumulatifs de toutes les transformations de matrice.

Supposons que deux matrices de transformation, rotation et translation, sont multipliées ensemble. Le résultat est une nouvelle matrice qui exécute les fonctions de rotation et de translation. Étant donné que la multiplication de matrice n’est pas commutative, une transformation de rotation multipliée par une transformation de translation est différente de la transformation de translation multipliée par la transformation de rotation.

Les exemples de code suivants montrent comment appliquer la rotation suivie de la traduction, puis la translation suivie d’une rotation. Notez que les résultats de rendu sont différents.


```C++
D2D1_RECT_F rectangle = D2D1::RectF(300.0f, 40.0f, 360.0f, 100.0f);

// Draw the rectangle before transforming the render target.

m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(330.0f, 70.0f)
    );


D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

// First rotate about the center of the square and then move
// 20 pixels to the right along the x-axis
// and 10 pixels downward along the y-axis.
m_pRenderTarget->SetTransform(rotation* translation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush, 1.0f);
```




```C++
D2D1_RECT_F rectangle = D2D1::Rect(40.0f, 40.0f, 100.0f, 100.0f);

// Draw a rectangle without transforming it.
m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

m_pRenderTarget->SetTransform(translation);

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(70.0f, 70.0f)
    );

// First move 20 pixels to the right along the x-axis and
// 10 pixels downward along the y-axis,
// and then rotate about the center of the original square.
m_pRenderTarget->SetTransform(translation * rotation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



Le code génère la sortie illustrée dans l’illustration suivante.

![illustration d’un rectangle qui a été traduit, puis pivoté et un rectangle qui a été pivoté, puis traduit](images/multipletransforms.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> <dt>

[Vue d’ensemble des transformations Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 




