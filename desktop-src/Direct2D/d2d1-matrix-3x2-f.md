---
title: D2D1_MATRIX_3X2_F (D2d1. h)
description: Représente une matrice 3 par 2.
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb252e35508c48570c96f251205fc8a54755687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510125"
---
# <a name="d2d1_matrix_3x2_f"></a><span data-ttu-id="99424-104">D2D1 \_ matrice \_ matrice \_ F</span><span class="sxs-lookup"><span data-stu-id="99424-104">D2D1\_MATRIX\_3X2\_F</span></span>

<span data-ttu-id="99424-105">Représente une matrice 3 par 2.</span><span class="sxs-lookup"><span data-stu-id="99424-105">Represents a 3-by-2 matrix.</span></span>


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a><span data-ttu-id="99424-106">Notes</span><span class="sxs-lookup"><span data-stu-id="99424-106">Remarks</span></span>

<span data-ttu-id="99424-107">**D2d1 \_ MATRIX \_ matrice** est un nouveau nom pour la [**structure \_ \_ matrice \_ F de la matrice D2D**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) .</span><span class="sxs-lookup"><span data-stu-id="99424-107">**D2D1\_MATRIX\_3X2** is a new name for the [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="99424-108">Pour obtenir la liste des champs fournis par la matrice, consultez la [**\_ matrice D2D \_ matrice \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span><span class="sxs-lookup"><span data-stu-id="99424-108">For a list of fields provided by the matrix, see [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span></span>

<span data-ttu-id="99424-109">Pour simplifier les opérations de matrice courantes, Direct2D fournit la classe [**d2d1 :: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) , qui est dérivée de la structure matrice de la [**\_ matrice \_ d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) .</span><span class="sxs-lookup"><span data-stu-id="99424-109">To simplify common matrix operations, Direct2D provides the [**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class, which is derived from the [**D2D1\_MATRIX\_3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="99424-110">La classe **Matrix3x2F** fournit un ensemble de méthodes d’assistance pour effectuer des tâches courantes, telles que la création d’une matrice de translation ou d’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="99424-110">The **Matrix3x2F** class provides a set of helper methods for performing common tasks, such as creating a translation or skew matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="99424-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="99424-111">Examples</span></span>

<span data-ttu-id="99424-112">L’exemple suivant utilise la méthode [**d2d1 :: Matrix3x2F :: rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) pour créer une matrice de rotation qui fait pivoter un carré dans le sens des aiguilles d’une montre à 45 degrés à propos du centre du carré et transmet la matrice à la méthode [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) de la cible de rendu (*m \_ pRenderTarget*).</span><span class="sxs-lookup"><span data-stu-id="99424-112">The following example uses the [**D2D1::Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method to create a rotation matrix that rotates a square clockwise 45 degrees about the center of the square and passes the matrix to the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of the render target (*m\_pRenderTarget*).</span></span>

<span data-ttu-id="99424-113">L’illustration suivante montre l’effet de l’application de la transformation de rotation précédente au carré.</span><span class="sxs-lookup"><span data-stu-id="99424-113">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="99424-114">Le carré d’origine est un contour en pointillés, et le carré pivoté est un contour Uni.</span><span class="sxs-lookup"><span data-stu-id="99424-114">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![illustration d’un carré pivoté dans le sens des aiguilles d’une montre à 45 degrés à propos du centre du carré d’origine](images/rotate-ovw.png)


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



<span data-ttu-id="99424-116">Le code a été omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="99424-116">Code has been omitted from this example.</span></span> <span data-ttu-id="99424-117">Pour plus d’informations sur les transformations, consultez [vue d’ensemble des transformations](direct2d-transforms-overview.md).</span><span class="sxs-lookup"><span data-stu-id="99424-117">For more information about transforms, see the [Transforms Overview](direct2d-transforms-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99424-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99424-118">Requirements</span></span>



| <span data-ttu-id="99424-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99424-119">Requirement</span></span> | <span data-ttu-id="99424-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="99424-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99424-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99424-121">Minimum supported client</span></span><br/> | <span data-ttu-id="99424-122">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="99424-122">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="99424-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99424-123">Minimum supported server</span></span><br/> | <span data-ttu-id="99424-124">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="99424-124">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="99424-125">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99424-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="99424-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="99424-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="99424-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="99424-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="99424-128"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="99424-128"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="99424-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99424-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99424-130">**D2D1::Matrix3x2F**</span><span class="sxs-lookup"><span data-stu-id="99424-130">**D2D1::Matrix3x2F**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[<span data-ttu-id="99424-131">Vue d’ensemble des transformations</span><span class="sxs-lookup"><span data-stu-id="99424-131">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="99424-132">Comment faire pivoter un objet</span><span class="sxs-lookup"><span data-stu-id="99424-132">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="99424-133">Mise à l’échelle d’un objet</span><span class="sxs-lookup"><span data-stu-id="99424-133">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="99424-134">Comment incliner un objet</span><span class="sxs-lookup"><span data-stu-id="99424-134">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="99424-135">Comment traduire un objet</span><span class="sxs-lookup"><span data-stu-id="99424-135">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="99424-136">**\_Matrice matrice \_ D2D \_ F**</span><span class="sxs-lookup"><span data-stu-id="99424-136">**D2D\_MATRIX\_3X2\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

