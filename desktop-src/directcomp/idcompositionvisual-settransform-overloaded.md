---
title: Méthodes IDCompositionVisual SetTransform (Dcomp. h)
description: Définit la propriété de transformation de cet visuel. La propriété transformer spécifie une transformation 2D utilisée pour modifier le système de coordonnées de cet visuel. La propriété peut spécifier une matrice de transformation 3 par 2 ou un objet de transformation.
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
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
ms.openlocfilehash: 00f5da890cd22c5c827a36062a0b0c3f9bc19cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317442"
---
# <a name="idcompositionvisualsettransform-methods"></a><span data-ttu-id="bad53-106">IDCompositionVisual :: SetTransform, méthodes</span><span class="sxs-lookup"><span data-stu-id="bad53-106">IDCompositionVisual::SetTransform methods</span></span>

<span data-ttu-id="bad53-107">Définit la propriété de transformation de cet visuel.</span><span class="sxs-lookup"><span data-stu-id="bad53-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="bad53-108">La propriété transformer spécifie une transformation 2D utilisée pour modifier le système de coordonnées de cet visuel.</span><span class="sxs-lookup"><span data-stu-id="bad53-108">The Transform property specifies a 2D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="bad53-109">La propriété peut spécifier une matrice de transformation 3 par 2 ou un objet de transformation.</span><span class="sxs-lookup"><span data-stu-id="bad53-109">The property can specify either a 3-by-2 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="bad53-110">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="bad53-110">Overload list</span></span>



| <span data-ttu-id="bad53-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="bad53-111">Method</span></span>                                                                                                    | <span data-ttu-id="bad53-112">Description</span><span class="sxs-lookup"><span data-stu-id="bad53-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="bad53-113">[**SetTransform ( \_ matrice D2D \_ matrice \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="bad53-113">[**SetTransform(D2D\_MATRIX\_3X2\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span></span>          | <span data-ttu-id="bad53-114">Définit la propriété de transformation sur la matrice de transformation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bad53-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="bad53-115">[**SetTransform (IDCompositionTransform \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span><span class="sxs-lookup"><span data-stu-id="bad53-115">[**SetTransform(IDCompositionTransform\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span></span> | <span data-ttu-id="bad53-116">Définit la propriété de transformation sur l’objet de transformation spécifié.</span><span class="sxs-lookup"><span data-stu-id="bad53-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bad53-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bad53-117">Requirements</span></span>



| <span data-ttu-id="bad53-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bad53-118">Requirement</span></span> | <span data-ttu-id="bad53-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bad53-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bad53-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bad53-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bad53-121">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bad53-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bad53-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bad53-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bad53-123">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bad53-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bad53-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bad53-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bad53-125"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bad53-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bad53-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bad53-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="bad53-127"><dt>Dcomp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bad53-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="bad53-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bad53-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bad53-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bad53-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bad53-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bad53-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad53-131">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="bad53-131">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="bad53-132">**IDCompositionRotateTransform**</span><span class="sxs-lookup"><span data-stu-id="bad53-132">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="bad53-133">**IDCompositionScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="bad53-133">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="bad53-134">**IDCompositionSkewTransform**</span><span class="sxs-lookup"><span data-stu-id="bad53-134">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="bad53-135">**IDCompositionTransform**</span><span class="sxs-lookup"><span data-stu-id="bad53-135">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="bad53-136">**IDCompositionTranslateTransform**</span><span class="sxs-lookup"><span data-stu-id="bad53-136">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="bad53-137">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="bad53-137">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="bad53-138">**IDCompositionVisual::SetOffsetX**</span><span class="sxs-lookup"><span data-stu-id="bad53-138">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="bad53-139">**IDCompositionVisual::SetOffsetY**</span><span class="sxs-lookup"><span data-stu-id="bad53-139">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="bad53-140">�</span><span class="sxs-lookup"><span data-stu-id="bad53-140">�</span></span>

<span data-ttu-id="bad53-141">�</span><span class="sxs-lookup"><span data-stu-id="bad53-141">�</span></span>
