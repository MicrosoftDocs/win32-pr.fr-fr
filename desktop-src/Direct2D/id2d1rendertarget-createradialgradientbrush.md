---
title: Méthodes ID2D1RenderTarget CreateRadialGradientBrush (D2d1. h)
description: Crée un objet ID2D1RadialGradientBrush qui peut être utilisé pour peindre des zones avec un dégradé radial.
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- Méthodes CreateRadialGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 680cc981943e45eb32834e48151f391f6249cc1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530447"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a><span data-ttu-id="93265-104">ID2D1RenderTarget :: CreateRadialGradientBrush, méthodes</span><span class="sxs-lookup"><span data-stu-id="93265-104">ID2D1RenderTarget::CreateRadialGradientBrush methods</span></span>

<span data-ttu-id="93265-105">Crée un objet [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) qui peut être utilisé pour peindre des zones avec un dégradé radial.</span><span class="sxs-lookup"><span data-stu-id="93265-105">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) object that can be used to paint areas with a radial gradient.</span></span>

### <a name="overload-list"></a><span data-ttu-id="93265-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="93265-106">Overload list</span></span>



| <span data-ttu-id="93265-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="93265-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="93265-108">Description</span><span class="sxs-lookup"><span data-stu-id="93265-108">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93265-109">[**CreateRadialGradientBrush ( \_ Propriétés du pinceau de dégradé radial D2D1 \_ \_ \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="93265-109">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span>                            | <span data-ttu-id="93265-110">Crée un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) qui contient les points de dégradé spécifiés, n’a aucune transformation et a une opacité de base de 1,0.</span><span class="sxs-lookup"><span data-stu-id="93265-110">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.</span></span> <br/> |
| <span data-ttu-id="93265-111">[**CreateRadialGradientBrush ( \_ Propriétés de pinceau de dégradé radial D2D1 \_ \_ \_&, \_ Propriétés de pinceau d2d1 \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="93265-111">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES&,D2D1\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span>   | <span data-ttu-id="93265-112">Crée un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) qui contient les points de dégradé spécifiés et a la transformation et l’opacité de base spécifiées.</span><span class="sxs-lookup"><span data-stu-id="93265-112">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |
| <span data-ttu-id="93265-113">[**CreateRadialGradientBrush ( \_ Propriétés de pinceau de dégradé radial d2d1 \_ \_ \_ \* , propriétés de \_ pinceau d2d1 \_ \* , ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="93265-113">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES\*,D2D1\_BRUSH\_PROPERTIES\*,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span> | <span data-ttu-id="93265-114">Crée un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) qui contient les points de dégradé spécifiés et a la transformation et l’opacité de base spécifiées.</span><span class="sxs-lookup"><span data-stu-id="93265-114">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="93265-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="93265-115">Examples</span></span>

<span data-ttu-id="93265-116">Pour obtenir un exemple, consultez [comment créer un pinceau de dégradé radial](how-to-create-a-radial-gradient-brush.md).</span><span class="sxs-lookup"><span data-stu-id="93265-116">For an example, see [How to Create a Radial Gradient Brush](how-to-create-a-radial-gradient-brush.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93265-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93265-117">Requirements</span></span>



| <span data-ttu-id="93265-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93265-118">Requirement</span></span> | <span data-ttu-id="93265-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="93265-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="93265-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="93265-120">Header</span></span><br/>  | <dl> <span data-ttu-id="93265-121"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="93265-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="93265-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="93265-122">Library</span></span><br/> | <dl> <span data-ttu-id="93265-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93265-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="93265-124">DLL</span><span class="sxs-lookup"><span data-stu-id="93265-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="93265-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93265-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93265-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93265-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93265-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="93265-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="93265-128">Comment créer un pinceau de dégradé radial</span><span class="sxs-lookup"><span data-stu-id="93265-128">How to Create a Radial Gradient Brush</span></span>](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="93265-129">Vue d’ensemble des pinceaux</span><span class="sxs-lookup"><span data-stu-id="93265-129">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

<span data-ttu-id="93265-130">�</span><span class="sxs-lookup"><span data-stu-id="93265-130">�</span></span>

<span data-ttu-id="93265-131">�</span><span class="sxs-lookup"><span data-stu-id="93265-131">�</span></span>
