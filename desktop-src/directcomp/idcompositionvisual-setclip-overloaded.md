---
title: IDCompositionVisual SetClip, méthodes (Dcomp. h)
description: Définit la propriété de découpage de ce visuel sur la zone rectangulaire ou l’objet clip spécifié.
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- SetClip, méthodes DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e421c916d305b95029bb6ffd8328346b4ea36918
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743412"
---
# <a name="idcompositionvisualsetclip-methods"></a><span data-ttu-id="a19ca-104">IDCompositionVisual :: SetClip, méthodes</span><span class="sxs-lookup"><span data-stu-id="a19ca-104">IDCompositionVisual::SetClip methods</span></span>

<span data-ttu-id="a19ca-105">Définit la propriété de découpage de ce visuel sur la zone rectangulaire ou l’objet clip spécifié.</span><span class="sxs-lookup"><span data-stu-id="a19ca-105">Sets the Clip property of this visual to the specified rectangular region or clip object.</span></span> <span data-ttu-id="a19ca-106">La propriété Clip restreint le rendu de la sous-arborescence visuelle qui est enracinée dans ce visuel à une région rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="a19ca-106">The Clip property restricts the rendering of the visual subtree that is rooted at this visual to a rectangular region.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a19ca-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="a19ca-107">Overload list</span></span>



| <span data-ttu-id="a19ca-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="a19ca-108">Method</span></span>                                                                                | <span data-ttu-id="a19ca-109">Description</span><span class="sxs-lookup"><span data-stu-id="a19ca-109">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span data-ttu-id="a19ca-110">[**SetClip (const D2D \_ rect \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="a19ca-110">[**SetClip(const D2D\_RECT\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span></span> | <span data-ttu-id="a19ca-111">Définit la propriété de la zone rectangulaire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a19ca-111">Sets the Clip property to the specified rectangular region.</span></span><br/> |
| <span data-ttu-id="a19ca-112">[**SetClip (IDCompositionClip \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span><span class="sxs-lookup"><span data-stu-id="a19ca-112">[**SetClip(IDCompositionClip\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span></span> | <span data-ttu-id="a19ca-113">Affecte l’objet clip spécifié à la propriété de la séquence.</span><span class="sxs-lookup"><span data-stu-id="a19ca-113">Sets the Clip property to the specified clip object.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="a19ca-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a19ca-114">Requirements</span></span>



| <span data-ttu-id="a19ca-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a19ca-115">Requirement</span></span> | <span data-ttu-id="a19ca-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a19ca-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a19ca-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a19ca-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a19ca-118">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a19ca-118">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a19ca-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a19ca-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a19ca-120">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a19ca-120">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a19ca-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a19ca-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a19ca-122"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a19ca-122"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a19ca-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a19ca-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a19ca-124"><dt>Dcomp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a19ca-124"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="a19ca-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a19ca-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a19ca-126"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a19ca-126"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a19ca-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a19ca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a19ca-128">Portion</span><span class="sxs-lookup"><span data-stu-id="a19ca-128">Clipping</span></span>](clipping.md)
</dt> <dt>

[<span data-ttu-id="a19ca-129">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="a19ca-129">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

<span data-ttu-id="a19ca-130">�</span><span class="sxs-lookup"><span data-stu-id="a19ca-130">�</span></span>

<span data-ttu-id="a19ca-131">�</span><span class="sxs-lookup"><span data-stu-id="a19ca-131">�</span></span>
