---
title: Méthodes ID2D1RenderTarget CreateLinearGradientBrush (D2d1. h)
description: Crée un objet ID2D1LinearGradientBrush pour peindre des zones avec un dégradé linéaire.
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- Méthodes CreateLinearGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 428fcb44ddf50af7b3e78c28e359430bceee2f79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523936"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a><span data-ttu-id="cc082-104">ID2D1RenderTarget :: CreateLinearGradientBrush, méthodes</span><span class="sxs-lookup"><span data-stu-id="cc082-104">ID2D1RenderTarget::CreateLinearGradientBrush methods</span></span>

<span data-ttu-id="cc082-105">Crée un objet [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) pour peindre des zones avec un dégradé linéaire.</span><span class="sxs-lookup"><span data-stu-id="cc082-105">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) object for painting areas with a linear gradient.</span></span>

### <a name="overload-list"></a><span data-ttu-id="cc082-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="cc082-106">Overload list</span></span>



| <span data-ttu-id="cc082-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="cc082-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="cc082-108">Description</span><span class="sxs-lookup"><span data-stu-id="cc082-108">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc082-109">[**CreateLinearGradientBrush ( \_ Propriétés de pinceau de dégradé linéaire D2D1 \_ \_ \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="cc082-109">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span>                            | <span data-ttu-id="cc082-110">Crée un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) qui contient les points de dégradé spécifiés, n’a aucune transformation et a une opacité de base de 1,0.</span><span class="sxs-lookup"><span data-stu-id="cc082-110">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.</span></span> <br/> |
| <span data-ttu-id="cc082-111">[**CreateLinearGradientBrush ( \_ Propriétés de pinceau de dégradé linéaire D2D1 \_ \_ \_&, \_ Propriétés de pinceau d2d1 \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="cc082-111">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES&,D2D1\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span>   | <span data-ttu-id="cc082-112">Crée un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) qui contient les points de dégradé spécifiés et a la transformation et l’opacité de base spécifiées.</span><span class="sxs-lookup"><span data-stu-id="cc082-112">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |
| <span data-ttu-id="cc082-113">[**CreateLinearGradientBrush ( \_ Propriétés de pinceau de dégradé linéaire d2d1 \_ \_ \_ \* , propriétés de \_ pinceau d2d1 \_ \* , ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="cc082-113">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES\*,D2D1\_BRUSH\_PROPERTIES\*,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span> | <span data-ttu-id="cc082-114">Crée un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) qui contient les points de dégradé spécifiés et a la transformation et l’opacité de base spécifiées.</span><span class="sxs-lookup"><span data-stu-id="cc082-114">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="cc082-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="cc082-115">Examples</span></span>

<span data-ttu-id="cc082-116">Pour obtenir un exemple qui montre comment créer une collection de points de dégradé et l’utiliser pour définir un dégradé linéaire, consultez [comment créer un pinceau de dégradé linéaire](how-to-create-a-linear-gradient-brush.md).</span><span class="sxs-lookup"><span data-stu-id="cc082-116">For an example showing how to create a gradient stop collection and use it to define a linear gradient, see [How to Create a Linear Gradient Brush](how-to-create-a-linear-gradient-brush.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc082-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc082-117">Requirements</span></span>



| <span data-ttu-id="cc082-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc082-118">Requirement</span></span> | <span data-ttu-id="cc082-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc082-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cc082-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc082-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cc082-121"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc082-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc082-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cc082-122">Library</span></span><br/> | <dl> <span data-ttu-id="cc082-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc082-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="cc082-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cc082-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="cc082-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc082-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc082-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc082-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc082-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="cc082-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="cc082-128">**CreateGradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="cc082-128">**CreateGradientStopCollection**</span></span>](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[<span data-ttu-id="cc082-129">**ID2D1GradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="cc082-129">**ID2D1GradientStopCollection**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[<span data-ttu-id="cc082-130">**ID2D1LinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="cc082-130">**ID2D1LinearGradientBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[<span data-ttu-id="cc082-131">**ID2D1RadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="cc082-131">**ID2D1RadialGradientBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[<span data-ttu-id="cc082-132">Comment créer un pinceau de dégradé linéaire</span><span class="sxs-lookup"><span data-stu-id="cc082-132">How to Create a Linear Gradient Brush</span></span>](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="cc082-133">Vue d’ensemble des pinceaux</span><span class="sxs-lookup"><span data-stu-id="cc082-133">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

<span data-ttu-id="cc082-134">�</span><span class="sxs-lookup"><span data-stu-id="cc082-134">�</span></span>

<span data-ttu-id="cc082-135">�</span><span class="sxs-lookup"><span data-stu-id="cc082-135">�</span></span>
