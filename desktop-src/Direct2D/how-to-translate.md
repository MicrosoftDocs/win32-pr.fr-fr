---
title: Comment traduire un objet
description: Montre comment traduire un objet.
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316086"
---
# <a name="how-to-translate-an-object"></a><span data-ttu-id="29b50-103">Comment traduire un objet</span><span class="sxs-lookup"><span data-stu-id="29b50-103">How to Translate an Object</span></span>

<span data-ttu-id="29b50-104">La conversion d’un objet 2D consiste à déplacer l’objet le long de l’axe x, de l’axe y, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="29b50-104">To translate a 2-D object is to move the object along the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="29b50-105">Vous pouvez appeler l’une des deux méthodes suivantes pour créer une transformation de traduction.</span><span class="sxs-lookup"><span data-stu-id="29b50-105">You can call either one of the following two methods to create a translation transformation.</span></span>

-   <span data-ttu-id="29b50-106">[**Translation (taille \_ d2d1 \_ F)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): prend une paire ordonnée qui définit la distance de translation le long de l’axe x et de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="29b50-106">[**Translation(D2D1\_SIZE\_F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): takes an ordered pair that defines the distance to translate along the x-axis and the y-axis.</span></span>
-   <span data-ttu-id="29b50-107">[**Translation (float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): prend la distance pour effectuer la translation le long de l’axe x et la distance pour la translation le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="29b50-107">[**Translation(float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): takes the distance to translate along the x-axis and the distance to translate along the y-axis.</span></span>

<span data-ttu-id="29b50-108">Le code suivant crée une matrice de transformation de translation qui déplace le carré de 20 unités vers la droite le long de l’axe x et de 10 unités vers le bas le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="29b50-108">The following code creates a translation transformation matrix that moves the square 20 units to the right along the x-axis and 10 units downward along the y-axis.</span></span>


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



<span data-ttu-id="29b50-109">L’illustration suivante montre l’effet de l’application de la transformation de translation au carré, où le carré d’origine est un contour en pointillés et le carré traduit est un contour Uni.</span><span class="sxs-lookup"><span data-stu-id="29b50-109">The following illustration shows the effect of applying the translation transformation to the square, where the original square is a dotted outline and the translated square is a solid outline.</span></span>

![illustration d’un carré déplacé de 20 unités vers la droite le long de l’axe x et de 10 unités vers le côté de l’axe y](images/translation-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="29b50-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29b50-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29b50-112">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="29b50-112">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="29b50-113">Vue d’ensemble des transformations Direct2D</span><span class="sxs-lookup"><span data-stu-id="29b50-113">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 