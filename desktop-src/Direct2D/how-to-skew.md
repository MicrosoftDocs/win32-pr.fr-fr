---
title: Comment incliner un objet
description: Montre comment incliner un objet.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691062e64d4255b1e2f7711b5ff700d72fd90063
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842598"
---
# <a name="how-to-skew-an-object"></a><span data-ttu-id="3a403-103">Comment incliner un objet</span><span class="sxs-lookup"><span data-stu-id="3a403-103">How to Skew an Object</span></span>

<span data-ttu-id="3a403-104">Pour incliner (ou cisailler) un objet signifie qu’il doit déformer un objet d’un angle spécifié par rapport à l’axe des x, à l’axe des y ou aux deux.</span><span class="sxs-lookup"><span data-stu-id="3a403-104">To skew (or shear) an object means to distort an object by a specified angle from the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="3a403-105">Par exemple, lorsque vous inclinez un carré, il devient un parallélogramme.</span><span class="sxs-lookup"><span data-stu-id="3a403-105">For example, when you skew a square, it becomes a parallelogram.</span></span>

<span data-ttu-id="3a403-106">La méthode [**Matrix3x2F :: skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) utilise 3 paramètres :</span><span class="sxs-lookup"><span data-stu-id="3a403-106">The [**Matrix3x2F::Skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) method takes 3 parameters:</span></span>

-   <span data-ttu-id="3a403-107">*AngleX*: angle d’inclinaison de l’axe x, mesuré en degrés dans le sens inverse des aiguilles d’une position à partir de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="3a403-107">*angleX*: The x-axis skew angle, which is measured in degrees counterclockwise from the y-axis.</span></span>
-   <span data-ttu-id="3a403-108">*AngleY*: angle d’inclinaison de l’axe y, mesuré en degrés dans le sens des aiguilles d’une montre à partir de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="3a403-108">*angleY*: The y-axis skew angle, which is measured in degrees clockwise from the x-axis.</span></span>
-   <span data-ttu-id="3a403-109">*centerPoint*: point sur lequel l’inclinaison est exécutée.</span><span class="sxs-lookup"><span data-stu-id="3a403-109">*centerPoint*: The point about which the skew is performed.</span></span>

<span data-ttu-id="3a403-110">Pour prédire l’effet d’une transformation d’inclinaison, prenez en compte que *AngleX* est l’angle d’inclinaison mesuré en degrés dans le sens inverse des aiguilles d’une position à partir de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="3a403-110">To predict the effect of a skew transformation, consider that *angleX* is the skew angle measured in degrees counterclockwise from the y-axis.</span></span> <span data-ttu-id="3a403-111">Par exemple, si *AngleX* a la valeur 30, l’objet passe à 30 degrés dans le sens inverse des aiguilles d’une montre sur l’axe y du *centerPoint*.</span><span class="sxs-lookup"><span data-stu-id="3a403-111">For example, if *angleX* is set to 30, the object skews 30 degrees counterclockwise along the y-axis about the *centerPoint*.</span></span> <span data-ttu-id="3a403-112">L’illustration suivante montre un décalage carré horizontal de 30 degrés par-dessus le coin supérieur gauche du carré.</span><span class="sxs-lookup"><span data-stu-id="3a403-112">The following illustration shows a square skewed horizontally 30 degrees about the upper-left corner of the square.</span></span>

![illustration d’un carré incliné de 30 degrés dans le sens inverse des aiguilles d’une montre à partir de l’axe y](images/skewx.png)

<span data-ttu-id="3a403-114">De même, *AngleY* est un angle d’inclinaison mesuré en degrés dans le sens des aiguilles d’une montre à partir de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="3a403-114">Similarly, *angleY* is a skew angle measured in degrees clockwise from the x-axis.</span></span> <span data-ttu-id="3a403-115">Par exemple, si *AngleY* est défini sur 30, l’objet passe à 30 degrés dans le sens horaire le long de l’axe x à propos du *centerPoint*.</span><span class="sxs-lookup"><span data-stu-id="3a403-115">For example, if *angleY* is set to 30, the object skews 30 degrees clockwise along the x-axis about the *centerPoint*.</span></span> <span data-ttu-id="3a403-116">L’illustration suivante montre un décalage carré vertical de 30 degrés par-dessus le coin supérieur gauche du carré.</span><span class="sxs-lookup"><span data-stu-id="3a403-116">The following illustration shows a square skewed vertically 30 degrees about the upper-left corner of the square.</span></span>

![illustration d’un carré incliné 30 degrés dans le sens des aiguilles d’une montre à partir de l’axe x](images/skewy.png)

<span data-ttu-id="3a403-118">Si vous définissez à la fois *AngleX* et *AngleY* sur 30 degrés, et *centerPoint* sur l’angle supérieur gauche du carré, vous verrez le carré incliné suivant (entouré d’une forme unie).</span><span class="sxs-lookup"><span data-stu-id="3a403-118">If you set both *angleX* and *angleY* to 30 degrees, and the *centerPoint* to the upper-left corner of the square, you will see the following skewed square (solid outlined).</span></span> <span data-ttu-id="3a403-119">Notez que le carré incliné est incliné de 30 degrés dans le sens inverse des aiguilles d’une montre à partir de l’axe y et de 30 degrés dans le sens des aiguilles d’une montre à partir de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="3a403-119">Notice that the skewed square is skewed 30 degrees counterclockwise from the y-axis and 30 degrees clockwise from the x-axis.</span></span>

![illustration d’un carré incliné de 30 degrés dans le sens inverse des aiguilles d’une montre à partir de l’axe y et de 30 degrés dans le sens horaire à partir de l’axe x](images/skewxy.png)

<span data-ttu-id="3a403-121">L’exemple de code suivant incline le carré de 45 degrés horizontalement autour de l’angle supérieur gauche du carré.</span><span class="sxs-lookup"><span data-stu-id="3a403-121">The following code example skews the square 45 degrees horizontally about the upper-left corner of the square.</span></span>


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



<span data-ttu-id="3a403-122">L’illustration suivante montre l’effet de l’application de la transformation d’inclinaison au carré, où le carré d’origine est un contour en pointillés et l’objet incliné (parallélogramme) est un contour solide.</span><span class="sxs-lookup"><span data-stu-id="3a403-122">The following illustration shows the effect of applying the skew transformation to the square, where the original square is a dotted outline and the skewed object (parallelogram) is a solid outline.</span></span> <span data-ttu-id="3a403-123">Notez que l’angle d’inclinaison est de 45 degrés dans le sens inverse des aiguilles d’une position à partir de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="3a403-123">Notice that the skew angle is 45 degrees counterclockwise from the y-axis.</span></span>

![illustration d’un carré incliné de 45 degrés dans le sens inverse des aiguilles d’une montre à partir de l’axe y](images/skew-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="3a403-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a403-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a403-126">Vue d’ensemble des transformations Direct2D</span><span class="sxs-lookup"><span data-stu-id="3a403-126">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="3a403-127">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="3a403-127">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 