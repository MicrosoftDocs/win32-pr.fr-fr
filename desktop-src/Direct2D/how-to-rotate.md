---
title: Comment faire pivoter un objet
description: Montre comment faire pivoter un objet.
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cd900a78ba4d81919df91b85fd97723172eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941188"
---
# <a name="how-to-rotate-an-object"></a><span data-ttu-id="8179a-103">Comment faire pivoter un objet</span><span class="sxs-lookup"><span data-stu-id="8179a-103">How to Rotate an Object</span></span>

<span data-ttu-id="8179a-104">Cette rubrique explique comment faire pivoter un objet à propos d’un point spécifié.</span><span class="sxs-lookup"><span data-stu-id="8179a-104">This topic describes how to rotate an object about a specified point.</span></span> <span data-ttu-id="8179a-105">Pour faire pivoter un objet, appelez la méthode [**Matrix3x2F :: rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) .</span><span class="sxs-lookup"><span data-stu-id="8179a-105">To rotate an object, call [**Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method.</span></span> <span data-ttu-id="8179a-106">Cette méthode prend deux paramètres, l’angle spécifié et le point central.</span><span class="sxs-lookup"><span data-stu-id="8179a-106">This method takes two parameters, the specified angle and the center point.</span></span> <span data-ttu-id="8179a-107">L’angle est un angle de rotation dans le sens des aiguilles d’une montre, en degrés, et le point central est le point sur lequel l’objet pivote.</span><span class="sxs-lookup"><span data-stu-id="8179a-107">The angle is a clockwise rotation angle in degrees, and the center point is the point about which the object rotates.</span></span> <span data-ttu-id="8179a-108">Le point central est exprimé dans le système de coordonnées de l’objet transformé.</span><span class="sxs-lookup"><span data-stu-id="8179a-108">The center point is expressed in the coordinate system of the object that is transformed.</span></span>

<span data-ttu-id="8179a-109">Par exemple, le code suivant fait pivoter un carré dans le sens des aiguilles d’une montre à 45 degrés autour du centre du carré.</span><span class="sxs-lookup"><span data-stu-id="8179a-109">For example, the following code rotates a square clockwise 45 degrees about the center of the square.</span></span>


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



<span data-ttu-id="8179a-110">L’illustration suivante montre l’effet de l’application de la transformation de rotation précédente au carré.</span><span class="sxs-lookup"><span data-stu-id="8179a-110">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="8179a-111">Le carré d’origine est un contour en pointillés, et le carré pivoté est un contour Uni.</span><span class="sxs-lookup"><span data-stu-id="8179a-111">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![illustration d’un carré pivoté dans le sens des aiguilles d’une montre à 45 degrés à propos du centre du carré d’origine](images/rotate-ovw.png)

<span data-ttu-id="8179a-113">L’illustration suivante montre l’effet de la rotation par le même angle sur un point central différent.</span><span class="sxs-lookup"><span data-stu-id="8179a-113">The following illustration shows the effect of rotating by the same angle about a different center point.</span></span> <span data-ttu-id="8179a-114">Notez que les objets pivotés se trouvent à des positions différentes par rapport à l’original.</span><span class="sxs-lookup"><span data-stu-id="8179a-114">Notice that the rotated objects are in different positions relative to the original.</span></span> <span data-ttu-id="8179a-115">Le carré à gauche est le résultat d’une rotation autour du centre du carré d’origine, tandis que le carré droit est le résultat d’une rotation autour de l’angle supérieur gauche du carré d’origine.</span><span class="sxs-lookup"><span data-stu-id="8179a-115">The left outlined square is the result of rotating about the center of the original square, and the right outlined square is the result of rotating about the upper-left corner of the original square.</span></span>

![illustration d’un carré pivoté dans le sens des aiguilles d’une montre à 45 degrés à propos d’un point central différent](images/translate-rotationcompare.png)

## <a name="related-topics"></a><span data-ttu-id="8179a-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8179a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8179a-118">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="8179a-118">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="8179a-119">Vue d’ensemble des transformations Direct2D</span><span class="sxs-lookup"><span data-stu-id="8179a-119">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 