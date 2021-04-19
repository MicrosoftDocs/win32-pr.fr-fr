---
title: Méthodes IDCompositionVisual3 SetTransform (Dcomp. h)
description: Définit la propriété de transformation de cet visuel. La propriété transformer spécifie une transformation 3D utilisée pour modifier le système de coordonnées de cet visuel. La propriété peut spécifier une matrice de transformation 4-par-4 ou un objet de transformation.
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
keywords:
- Méthodes SetTransform DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 50237d4bbc8504a6bdcc9650f6c02dbdc30d093c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510967"
---
# <a name="idcompositionvisual3settransform-methods"></a><span data-ttu-id="9fa8f-106">IDCompositionVisual3 :: SetTransform, méthodes</span><span class="sxs-lookup"><span data-stu-id="9fa8f-106">IDCompositionVisual3::SetTransform methods</span></span>

<span data-ttu-id="9fa8f-107">Définit la propriété de transformation de cet visuel.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="9fa8f-108">La propriété transformer spécifie une transformation 3D utilisée pour modifier le système de coordonnées de cet visuel.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-108">The Transform property specifies a 3D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="9fa8f-109">La propriété peut spécifier une matrice de transformation 4-par-4 ou un objet de transformation.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-109">The property can specify either a 4-by-4 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="9fa8f-110">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="9fa8f-110">Overload list</span></span>



| <span data-ttu-id="9fa8f-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="9fa8f-111">Method</span></span>                                                                                  | <span data-ttu-id="9fa8f-112">Description</span><span class="sxs-lookup"><span data-stu-id="9fa8f-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="9fa8f-113">[**SetTransform ( \_ matrice D2D \_ 4x4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span><span class="sxs-lookup"><span data-stu-id="9fa8f-113">[**SetTransform(D2D\_MATRIX\_4X4\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span></span>       | <span data-ttu-id="9fa8f-114">Définit la propriété de transformation sur la matrice de transformation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="9fa8f-115">[**SetTransform (IDCompositionTransform3D \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span><span class="sxs-lookup"><span data-stu-id="9fa8f-115">[**SetTransform(IDCompositionTransform3D\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span></span> | <span data-ttu-id="9fa8f-116">Définit la propriété de transformation sur l’objet de transformation spécifié.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9fa8f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fa8f-117">Requirements</span></span>



| <span data-ttu-id="9fa8f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fa8f-118">Requirement</span></span> | <span data-ttu-id="9fa8f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fa8f-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa8f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fa8f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9fa8f-121">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fa8f-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9fa8f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fa8f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9fa8f-123">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fa8f-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9fa8f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9fa8f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fa8f-125"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fa8f-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9fa8f-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9fa8f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="9fa8f-127"><dt>Dcomp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fa8f-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="9fa8f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9fa8f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fa8f-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fa8f-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fa8f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fa8f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa8f-131">**IDCompositionVisual3**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-131">**IDCompositionVisual3**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

[<span data-ttu-id="9fa8f-132">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-132">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="9fa8f-133">**IDCompositionRotateTransform**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-133">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="9fa8f-134">**IDCompositionScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-134">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="9fa8f-135">**IDCompositionSkewTransform**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-135">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="9fa8f-136">**IDCompositionTransform**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-136">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="9fa8f-137">**IDCompositionTranslateTransform**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-137">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="9fa8f-138">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-138">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="9fa8f-139">**IDCompositionVisual::SetOffsetX**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-139">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="9fa8f-140">**IDCompositionVisual::SetOffsetY**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-140">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="9fa8f-141">�</span><span class="sxs-lookup"><span data-stu-id="9fa8f-141">�</span></span>

<span data-ttu-id="9fa8f-142">�</span><span class="sxs-lookup"><span data-stu-id="9fa8f-142">�</span></span>
