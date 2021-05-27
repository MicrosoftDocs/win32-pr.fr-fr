---
title: Méthodes ID2D1RenderTarget CreateGradientStopCollection (D2d1 \_ 1. h)
description: Crée un ID2D1GradientStopCollection à partir du tableau spécifié de \_ structures de point de dégradé d2d1 \_ .
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- Méthodes CreateGradientStopCollection Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: f099c1c71015ca433299843d388085103571d31d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549414"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a><span data-ttu-id="31264-104">ID2D1RenderTarget :: CreateGradientStopCollection, méthodes</span><span class="sxs-lookup"><span data-stu-id="31264-104">ID2D1RenderTarget::CreateGradientStopCollection methods</span></span>

<span data-ttu-id="31264-105">Crée un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) à partir du tableau spécifié de structures de [**\_ \_ point de dégradé d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="31264-105">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures.</span></span>

### <a name="overload-list"></a><span data-ttu-id="31264-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="31264-106">Overload list</span></span>



| <span data-ttu-id="31264-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="31264-107">Method</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="31264-108">Description</span><span class="sxs-lookup"><span data-stu-id="31264-108">Description</span></span>                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31264-109">**CreateGradientStopCollection (D2D1 \_ \_ Stop \* , D2D1 \_ gamma, d2d1 \_ mode Extend \_ , ID2D1GradientStopCollection \* \* )**</span><span class="sxs-lookup"><span data-stu-id="31264-109">**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,D2D1\_GAMMA,D2D1\_EXTEND\_MODE,ID2D1GradientStopCollection\*\*)**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) | <span data-ttu-id="31264-110">Crée un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) à partir des points de dégradé, du gamma d’interpolation de couleur et du mode extension spécifiés.</span><span class="sxs-lookup"><span data-stu-id="31264-110">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops, color interpolation gamma, and extend mode.</span></span> <br/>                                                              |
| [<span data-ttu-id="31264-111">**CreateGradientStopCollection (D2D1 \_ point \_ \* de dégradé, ID2D1GradientStopCollection \* \* )**</span><span class="sxs-lookup"><span data-stu-id="31264-111">**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,ID2D1GradientStopCollection\*\*)**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)                                                            | <span data-ttu-id="31264-112">Crée un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) à partir des points de dégradé spécifiés qui utilisent la gamma de l’interpolation de couleur [**d2d1 \_ gamma \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) et le mode d’extension de la bride.</span><span class="sxs-lookup"><span data-stu-id="31264-112">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops that uses the [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) color interpolation gamma and the clamp extend mode.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="31264-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="31264-113">Examples</span></span>

<span data-ttu-id="31264-114">L’exemple suivant crée un tableau de points de dégradé, puis les utilise pour créer un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span><span class="sxs-lookup"><span data-stu-id="31264-114">The following example creates an array of gradient stops, then uses them to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



<span data-ttu-id="31264-115">L’exemple de code suivant utilise [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) pour créer un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="31264-115">The next code example uses the [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to create an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span>


```C++
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
}
```



## <a name="requirements"></a><span data-ttu-id="31264-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="31264-116">Requirements</span></span>



| <span data-ttu-id="31264-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31264-117">Requirement</span></span> | <span data-ttu-id="31264-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="31264-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31264-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="31264-119">Header</span></span><br/>  | <dl> <span data-ttu-id="31264-120"><dt>D2d1 \_ 1. h (inclure D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31264-120"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="31264-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="31264-121">Library</span></span><br/> | <dl> <span data-ttu-id="31264-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31264-122"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="31264-123">DLL</span><span class="sxs-lookup"><span data-stu-id="31264-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="31264-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31264-124"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="31264-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31264-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31264-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="31264-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="31264-127">**\_Point de dégradé d2d1 \_**</span><span class="sxs-lookup"><span data-stu-id="31264-127">**D2D1\_GRADIENT\_STOP**</span></span>](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[<span data-ttu-id="31264-128">Comment créer un pinceau de dégradé linéaire</span><span class="sxs-lookup"><span data-stu-id="31264-128">How to Create a Linear Gradient Brush</span></span>](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="31264-129">Comment créer un pinceau de dégradé radial</span><span class="sxs-lookup"><span data-stu-id="31264-129">How to Create a Radial Gradient Brush</span></span>](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="31264-130">Vue d’ensemble des pinceaux</span><span class="sxs-lookup"><span data-stu-id="31264-130">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>