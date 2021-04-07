---
title: Comment appliquer plusieurs transformations à un objet
description: Montre comment appliquer plusieurs transformations à un objet.
ms.assetid: a3875072-bb73-4698-944e-102ab5539d80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e031a46545c59513767ed4d260be9dc677b3fb77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671774"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a><span data-ttu-id="e8243-103">Comment appliquer plusieurs transformations à un objet</span><span class="sxs-lookup"><span data-stu-id="e8243-103">How to Apply Multiple Transforms to an Object</span></span>

<span data-ttu-id="e8243-104">Pour effectuer plusieurs transformations sur un objet, vous pouvez combiner plusieurs transformations en une seule.</span><span class="sxs-lookup"><span data-stu-id="e8243-104">To perform multiple transforms on an object means to combine several transforms into one.</span></span> <span data-ttu-id="e8243-105">Autrement dit, en prenant la sortie de chaque matrice de transformation et en l’utilisant comme entrée pour la suivante, en obtenant les effets cumulatifs de toutes les transformations de matrice.</span><span class="sxs-lookup"><span data-stu-id="e8243-105">That is, taking the output from each transformation matrix and using it as the input for the next, thereby getting the cumulative effects of all the matrix transformations.</span></span>

<span data-ttu-id="e8243-106">Supposons que deux matrices de transformation, rotation et translation, sont multipliées ensemble.</span><span class="sxs-lookup"><span data-stu-id="e8243-106">Suppose two transformation matrices, rotation and translation, are multiplied together.</span></span> <span data-ttu-id="e8243-107">Le résultat est une nouvelle matrice qui exécute les fonctions de rotation et de translation.</span><span class="sxs-lookup"><span data-stu-id="e8243-107">The result is a new matrix that performs the functions of both rotation and translation.</span></span> <span data-ttu-id="e8243-108">Étant donné que la multiplication de matrice n’est pas commutative, une transformation de rotation multipliée par une transformation de translation est différente de la transformation de translation multipliée par la transformation de rotation.</span><span class="sxs-lookup"><span data-stu-id="e8243-108">Because matrix multiplication is not commutative, a rotation transformation multiplied by a translation transformation is different from the translation transformation multiplied by the rotation transformation.</span></span>

<span data-ttu-id="e8243-109">Les exemples de code suivants montrent comment appliquer la rotation suivie de la traduction, puis la translation suivie d’une rotation.</span><span class="sxs-lookup"><span data-stu-id="e8243-109">The following code examples show how to apply rotation followed by translation, and then translation followed by rotation.</span></span> <span data-ttu-id="e8243-110">Notez que les résultats de rendu sont différents.</span><span class="sxs-lookup"><span data-stu-id="e8243-110">Notice that the rendering results are different.</span></span>


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



<span data-ttu-id="e8243-111">Le code génère la sortie illustrée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="e8243-111">The code produces the output shown in the following illustration.</span></span>

![illustration d’un rectangle qui a été traduit, puis pivoté et un rectangle qui a été pivoté, puis traduit](images/multipletransforms.png)

## <a name="related-topics"></a><span data-ttu-id="e8243-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8243-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8243-114">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="e8243-114">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="e8243-115">Vue d’ensemble des transformations Direct2D</span><span class="sxs-lookup"><span data-stu-id="e8243-115">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 




