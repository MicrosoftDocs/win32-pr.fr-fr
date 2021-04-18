---
title: Méthodes ID2D1RenderTarget SetTransform
description: Applique la transformation spécifiée à la cible de rendu, en remplaçant la transformation existante. Toutes les opérations de dessin suivantes se produisent dans l’espace transformé.
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- Méthodes SetTransform Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 8310bf9e5c97beb3ea3cf3b2a9a513f606079a18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526482"
---
# <a name="id2d1rendertargetsettransform-methods"></a><span data-ttu-id="21e0e-105">ID2D1RenderTarget :: SetTransform, méthodes</span><span class="sxs-lookup"><span data-stu-id="21e0e-105">ID2D1RenderTarget::SetTransform methods</span></span>

<span data-ttu-id="21e0e-106">Applique la transformation spécifiée à la cible de rendu, en remplaçant la transformation existante.</span><span class="sxs-lookup"><span data-stu-id="21e0e-106">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="21e0e-107">Toutes les opérations de dessin suivantes se produisent dans l’espace transformé.</span><span class="sxs-lookup"><span data-stu-id="21e0e-107">All subsequent drawing operations occur in the transformed space.</span></span>

### <a name="overload-list"></a><span data-ttu-id="21e0e-108">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="21e0e-108">Overload list</span></span>



| <span data-ttu-id="21e0e-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="21e0e-109">Method</span></span>                                                                                              | <span data-ttu-id="21e0e-110">Description</span><span class="sxs-lookup"><span data-stu-id="21e0e-110">Description</span></span>                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21e0e-111">[**SetTransform (D2D1 \_ Matrix \_ matrice \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="21e0e-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="21e0e-112">Applique la transformation spécifiée à la cible de rendu, en remplaçant la transformation existante.</span><span class="sxs-lookup"><span data-stu-id="21e0e-112">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="21e0e-113">Toutes les opérations de dessin suivantes se produisent dans l’espace transformé.</span><span class="sxs-lookup"><span data-stu-id="21e0e-113">All subsequent drawing operations occur in the transformed space.</span></span> <br/> |
| <span data-ttu-id="21e0e-114">[**SetTransform (D2D1 \_ Matrix \_ matrice \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="21e0e-114">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="21e0e-115">Applique la transformation spécifiée à la cible de rendu, en remplaçant la transformation existante.</span><span class="sxs-lookup"><span data-stu-id="21e0e-115">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="21e0e-116">Toutes les opérations de dessin suivantes se produisent dans l’espace transformé.</span><span class="sxs-lookup"><span data-stu-id="21e0e-116">All subsequent drawing operations occur in the transformed space.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="21e0e-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="21e0e-117">Examples</span></span>

<span data-ttu-id="21e0e-118">L’exemple suivant utilise la méthode **setTransform** pour appliquer une rotation à la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="21e0e-118">The following example uses the **SetTransform** method to apply a rotation to the render target.</span></span> <span data-ttu-id="21e0e-119">Pour obtenir un exemple complet, consultez [Comment faire pivoter un objet](how-to-rotate.md).</span><span class="sxs-lookup"><span data-stu-id="21e0e-119">For the complete example, see [How to Rotate an Object](how-to-rotate.md).</span></span>


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



<span data-ttu-id="21e0e-120">Pour obtenir des exemples supplémentaires montrant comment transformer une cible de rendu, consultez [Comment mettre à l’échelle un objet](how-to-scale.md), [comment incliner un](how-to-skew.md)objet et [Comment convertir un objet](how-to-translate.md).</span><span class="sxs-lookup"><span data-stu-id="21e0e-120">For additional examples showing how to transform a render target, see [How to Scale an Object](how-to-scale.md), [How to Skew an Object](how-to-skew.md), and [How to Translate an Object](how-to-translate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21e0e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21e0e-121">Requirements</span></span>



| <span data-ttu-id="21e0e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21e0e-122">Requirement</span></span> | <span data-ttu-id="21e0e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="21e0e-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="21e0e-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="21e0e-124">Library</span></span><br/> | <dl> <span data-ttu-id="21e0e-125"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21e0e-125"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="21e0e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="21e0e-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="21e0e-127"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21e0e-127"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21e0e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21e0e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21e0e-129">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="21e0e-129">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="21e0e-130">Vue d’ensemble des transformations</span><span class="sxs-lookup"><span data-stu-id="21e0e-130">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="21e0e-131">Comment faire pivoter un objet</span><span class="sxs-lookup"><span data-stu-id="21e0e-131">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="21e0e-132">Mise à l’échelle d’un objet</span><span class="sxs-lookup"><span data-stu-id="21e0e-132">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="21e0e-133">Comment incliner un objet</span><span class="sxs-lookup"><span data-stu-id="21e0e-133">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="21e0e-134">Comment traduire un objet</span><span class="sxs-lookup"><span data-stu-id="21e0e-134">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="21e0e-135">Comment appliquer plusieurs transformations à un objet</span><span class="sxs-lookup"><span data-stu-id="21e0e-135">How to Apply Multiple Transforms to an Object</span></span>](how-to-apply-multiple-transforms.md)
</dt> </dl>

 

