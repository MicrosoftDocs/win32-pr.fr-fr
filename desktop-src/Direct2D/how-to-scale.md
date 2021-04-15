---
title: Mise à l’échelle d’un objet
description: Montre comment mettre à l’échelle un objet.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f46ae37197cb7cbfeb3f86588e1b5298cfc467
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463502"
---
# <a name="how-to-scale-an-object"></a><span data-ttu-id="0179e-103">Mise à l’échelle d’un objet</span><span class="sxs-lookup"><span data-stu-id="0179e-103">How to Scale an Object</span></span>

<span data-ttu-id="0179e-104">Cette rubrique explique comment mettre à l’échelle un objet à l’aide de la classe [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="0179e-104">This topic describes how to scale an object by using the [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="0179e-105">La mise à l’échelle d’un objet signifie que l’objet est plus grand ou plus petit.</span><span class="sxs-lookup"><span data-stu-id="0179e-105">To scale an object means to make the object larger or smaller.</span></span> <span data-ttu-id="0179e-106">Vous pouvez appeler l’une des deux méthodes suivantes pour mettre à l’échelle un objet.</span><span class="sxs-lookup"><span data-stu-id="0179e-106">You can call one of the following two methods to scale an object.</span></span>

-   <span data-ttu-id="0179e-107">**Matrix3x2F :: Scale (D2D1 \_ taille \_ F SCALEFACTOR, d2d1 \_ point \_ 2F Centerpoint)**</span><span class="sxs-lookup"><span data-stu-id="0179e-107">**Matrix3x2F::Scale(D2D1\_SIZE\_F scalefactor, D2D1\_POINT\_2F centerpoint)**</span></span>
-   <span data-ttu-id="0179e-108">**Matrix3x2F :: Scale (float ScaleX, float ScaleY, D2D1 \_ point \_ 2F Centerpoint)**</span><span class="sxs-lookup"><span data-stu-id="0179e-108">**Matrix3x2F::Scale(float scalex, float scaley, D2D1\_POINT\_2F centerpoint)**</span></span>

<span data-ttu-id="0179e-109">La première méthode stocke *ScaleX* et *ScaleY* en tant que paire ordonnée de valeurs à virgule flottante dans la structure [**d2d1 \_ size \_ F**](/windows/desktop/Direct2D/d2d1-size-f) .</span><span class="sxs-lookup"><span data-stu-id="0179e-109">The first method stores *scalex* and *scaley* as an ordered pair of floating-point values in the [**D2D1\_SIZE\_F**](/windows/desktop/Direct2D/d2d1-size-f) structure.</span></span> <span data-ttu-id="0179e-110">La deuxième méthode définit *ScaleX* et *ScaleY* en tant que paramètres individuels.</span><span class="sxs-lookup"><span data-stu-id="0179e-110">The second method defines *scalex* and *scaley* as individual parameters.</span></span>

<span data-ttu-id="0179e-111">Quelle que soit la méthode utilisée, vous devez spécifier des facteurs *ScaleX* et *ScaleY* .</span><span class="sxs-lookup"><span data-stu-id="0179e-111">Regardless of which method that you use, you must specify both *scalex* and *scaley* factors.</span></span> <span data-ttu-id="0179e-112">La valeur *ScaleX* est le facteur d’échelle sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="0179e-112">The *scalex* value is the scale factor in the x direction.</span></span> <span data-ttu-id="0179e-113">Par exemple, une valeur *ScaleX* de 1,5 étire l’objet à 150% le long de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="0179e-113">For example, a *scalex* value of 1.5 stretches the object to 150 percent along the x-axis.</span></span> <span data-ttu-id="0179e-114">De même, la valeur *ScaleY* est le facteur d’échelle sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="0179e-114">Similarly, the *scaley* value is the scale factor in the y direction.</span></span> <span data-ttu-id="0179e-115">Par exemple, une valeur *ScaleY* de 0,5 réduit la hauteur de l’objet de 50% le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="0179e-115">For example, a *scaley* value of 0.5 shrinks the height of the object by 50 percent along the y-axis.</span></span>

<span data-ttu-id="0179e-116">Pour spécifier un point comme centre de l’opération de mise à l’échelle, utilisez le paramètre *Centerpoint* .</span><span class="sxs-lookup"><span data-stu-id="0179e-116">To specify a point as the center of the scaling operation, use the *centerpoint* parameter.</span></span> <span data-ttu-id="0179e-117">Par défaut, un objet est centré sur son origine (0, 0).</span><span class="sxs-lookup"><span data-stu-id="0179e-117">By default, an object is centered about its origin (0,0).</span></span>

<span data-ttu-id="0179e-118">L’exemple de code suivant crée une transformation d’échelle pour augmenter la taille d’un carré à 130% de sa taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="0179e-118">The following example code creates a scale transformation to increase the size of a square to 130% of its original size.</span></span> <span data-ttu-id="0179e-119">Le *Centerpoint* est défini comme étant l’angle supérieur gauche du carré d’origine.</span><span class="sxs-lookup"><span data-stu-id="0179e-119">The *centerpoint* is set to be the upper-left corner of the original square.</span></span>


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



<span data-ttu-id="0179e-120">L’illustration suivante montre l’effet de l’application de la transformation d’échelle au carré.</span><span class="sxs-lookup"><span data-stu-id="0179e-120">The following illustration shows the effect of applying the scale transformation to the square.</span></span> <span data-ttu-id="0179e-121">Le carré d’origine est un contour en pointillés et le carré mis à l’échelle est un contour plein.</span><span class="sxs-lookup"><span data-stu-id="0179e-121">The original square is a dotted outline and the scaled square is a solid outline.</span></span>

![illustration du redimensionnement du carré à 130% de sa taille d’origine](images/scale-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="0179e-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0179e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0179e-124">Vue d’ensemble des transformations Direct2D</span><span class="sxs-lookup"><span data-stu-id="0179e-124">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="0179e-125">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="0179e-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 