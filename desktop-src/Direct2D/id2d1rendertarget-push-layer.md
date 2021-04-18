---
title: Méthodes ID2D1RenderTarget PushLayer (D2d1 \_ 1. h)
description: Ajoute la couche spécifiée à la cible de rendu afin qu’elle reçoive toutes les opérations de dessin suivantes jusqu’à ce que PopLayer soit appelé.
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- Méthodes PushLayer Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6a5609192162ae0b0c0e2af8f1b84429d8710509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533484"
---
# <a name="id2d1rendertargetpushlayer-methods"></a><span data-ttu-id="99d75-104">ID2D1RenderTarget ::P méthodes ushLayer</span><span class="sxs-lookup"><span data-stu-id="99d75-104">ID2D1RenderTarget::PushLayer methods</span></span>

<span data-ttu-id="99d75-105">Ajoute la couche spécifiée à la cible de rendu afin qu’elle reçoive toutes les opérations de dessin suivantes jusqu’à ce que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) soit appelé.</span><span class="sxs-lookup"><span data-stu-id="99d75-105">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span>

### <a name="overload-list"></a><span data-ttu-id="99d75-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="99d75-106">Overload list</span></span>



| <span data-ttu-id="99d75-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="99d75-107">Method</span></span>                                                                                                                            | <span data-ttu-id="99d75-108">Description</span><span class="sxs-lookup"><span data-stu-id="99d75-108">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99d75-109">[**PushLayer (paramètres de la \_ couche D2D1 \_&, ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="99d75-109">[**PushLayer(D2D1\_LAYER\_PARAMETERS&,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span></span>  | <span data-ttu-id="99d75-110">Ajoute la couche spécifiée à la cible de rendu afin qu’elle reçoive toutes les opérations de dessin suivantes jusqu’à ce que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) soit appelé.</span><span class="sxs-lookup"><span data-stu-id="99d75-110">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |
| <span data-ttu-id="99d75-111">[**PushLayer ( \_ paramètres de couche d2d1 \_ \* , ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="99d75-111">[**PushLayer(D2D1\_LAYER\_PARAMETERS\*,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span></span> | <span data-ttu-id="99d75-112">Ajoute la couche spécifiée à la cible de rendu afin qu’elle reçoive toutes les opérations de dessin suivantes jusqu’à ce que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) soit appelé.</span><span class="sxs-lookup"><span data-stu-id="99d75-112">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="99d75-113">Notes</span><span class="sxs-lookup"><span data-stu-id="99d75-113">Remarks</span></span>

<span data-ttu-id="99d75-114">La méthode [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) permet à un appelant de commencer à rediriger le rendu vers une couche.</span><span class="sxs-lookup"><span data-stu-id="99d75-114">The [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method enables a caller to begin redirecting rendering to a layer.</span></span> <span data-ttu-id="99d75-115">Toutes les opérations de rendu sont valides dans une couche.</span><span class="sxs-lookup"><span data-stu-id="99d75-115">All rendering operations are valid in a layer.</span></span> <span data-ttu-id="99d75-116">L’emplacement de la couche est affecté par le jeu de transformations universelles sur la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="99d75-116">The location of the layer is affected by the world transform set on the render target.</span></span>

<span data-ttu-id="99d75-117">Chaque **PushLayer** doit avoir un appel [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) correspondant.</span><span class="sxs-lookup"><span data-stu-id="99d75-117">Each **PushLayer** must have a matching [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) call.</span></span> <span data-ttu-id="99d75-118">S’il y a plus d’appels **PopLayer** que d’appels **PushLayer** , la cible de rendu est placée dans un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="99d75-118">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="99d75-119">Si [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) est appelé avant que toutes les couches en suspens soient dépilées, la cible de rendu est placée dans un état d’erreur et une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="99d75-119">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state, and an error is returned.</span></span> <span data-ttu-id="99d75-120">L’état d’erreur peut être effacé par un appel à [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="99d75-120">The error state can be cleared by a call to [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

<span data-ttu-id="99d75-121">Une ressource [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) particulière ne peut être active qu’en même temps.</span><span class="sxs-lookup"><span data-stu-id="99d75-121">A particular [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) resource can be active only at one time.</span></span> <span data-ttu-id="99d75-122">En d’autres termes, vous ne pouvez pas appeler une méthode [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) , puis suivre immédiatement une autre méthode **PushLayer** avec la même ressource de couche.</span><span class="sxs-lookup"><span data-stu-id="99d75-122">In other words, you cannot call a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method, and then immediately follow with another **PushLayer** method with the same layer resource.</span></span> <span data-ttu-id="99d75-123">Au lieu de cela, vous devez appeler la deuxième méthode **PushLayer** avec des ressources de couche différentes.</span><span class="sxs-lookup"><span data-stu-id="99d75-123">Instead, you must call the second **PushLayer** method with different layer resources.</span></span>

<span data-ttu-id="99d75-124">Pour obtenir un exemple, consultez [Comment découper une région avec des couches](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="99d75-124">For an example, see [How to Clip a Region with Layers](how-to-clip-with-layers.md).</span></span>

<span data-ttu-id="99d75-125">Cette méthode ne retourne pas de code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="99d75-125">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="99d75-126">Pour déterminer si une opération de dessin (telle que **PushLayer**) a échoué, vérifiez le résultat retourné par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="99d75-126">To determine whether a drawing operation (such as **PushLayer**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="99d75-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="99d75-127">Examples</span></span>

<span data-ttu-id="99d75-128">L’exemple suivant utilise une couche pour découper une image bitmap en un masque géométrique.</span><span class="sxs-lookup"><span data-stu-id="99d75-128">The following example uses a layer to clip a bitmap to a geometric mask.</span></span> <span data-ttu-id="99d75-129">Pour obtenir un exemple complet, consultez [Comment découper un masque géométrique](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="99d75-129">For the complete example, see [How to Clip to a Geometric Mask](how-to-clip-with-layers.md).</span></span>


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &amp;pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&amp;pLayer);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="99d75-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99d75-130">Requirements</span></span>



| <span data-ttu-id="99d75-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99d75-131">Requirement</span></span> | <span data-ttu-id="99d75-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="99d75-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99d75-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="99d75-133">Header</span></span><br/>  | <dl> <span data-ttu-id="99d75-134"><dt>D2d1 \_ 1. h (inclure D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99d75-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="99d75-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99d75-135">Library</span></span><br/> | <dl> <span data-ttu-id="99d75-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99d75-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="99d75-137">DLL</span><span class="sxs-lookup"><span data-stu-id="99d75-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="99d75-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99d75-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="99d75-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99d75-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99d75-140">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="99d75-140">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="99d75-141">Vue d’ensemble des couches</span><span class="sxs-lookup"><span data-stu-id="99d75-141">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

<span data-ttu-id="99d75-142">�</span><span class="sxs-lookup"><span data-stu-id="99d75-142">�</span></span>

<span data-ttu-id="99d75-143">�</span><span class="sxs-lookup"><span data-stu-id="99d75-143">�</span></span>
