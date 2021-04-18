---
title: Méthodes ID2D1RenderTarget CreateLayer (D2d1. h)
description: Crée une ressource de couche qui peut être utilisée avec cette cible de rendu et ses cibles de rendu compatibles.
ms.assetid: 074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7
keywords:
- Méthodes CreateLayer Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6e7fe86f041a818db77c28ed9461d8c8fb48ad64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540219"
---
# <a name="id2d1rendertargetcreatelayer-methods"></a><span data-ttu-id="638d0-104">ID2D1RenderTarget :: CreateLayer, méthodes</span><span class="sxs-lookup"><span data-stu-id="638d0-104">ID2D1RenderTarget::CreateLayer methods</span></span>

<span data-ttu-id="638d0-105">Crée une ressource de couche qui peut être utilisée avec cette cible de rendu et ses cibles de rendu compatibles.</span><span class="sxs-lookup"><span data-stu-id="638d0-105">Creates a layer resource that can be used with this render target and its compatible render targets.</span></span>

### <a name="overload-list"></a><span data-ttu-id="638d0-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="638d0-106">Overload list</span></span>



| <span data-ttu-id="638d0-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="638d0-107">Method</span></span>                                                                                                                 | <span data-ttu-id="638d0-108">Description</span><span class="sxs-lookup"><span data-stu-id="638d0-108">Description</span></span>                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="638d0-109">[**CreateLayer (ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="638d0-109">[**CreateLayer(ID2D1Layer\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))</span></span>                                | <span data-ttu-id="638d0-110">Crée une ressource de couche qui peut être utilisée avec cette cible de rendu et ses cibles de rendu compatibles.</span><span class="sxs-lookup"><span data-stu-id="638d0-110">Creates a layer resource that can be used with this render target and its compatible render targets.</span></span> <br/>                                               |
| <span data-ttu-id="638d0-111">[**CreateLayer (D2D1 \_ taille \_ F, ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="638d0-111">[**CreateLayer(D2D1\_SIZE\_F,ID2D1Layer\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))</span></span>       | <span data-ttu-id="638d0-112">Crée une ressource de couche qui peut être utilisée avec cette cible de rendu et ses cibles de rendu compatibles.</span><span class="sxs-lookup"><span data-stu-id="638d0-112">Creates a layer resource that can be used with this render target and its compatible render targets.</span></span> <span data-ttu-id="638d0-113">La nouvelle couche a la taille initiale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="638d0-113">The new layer has the specified initial size.</span></span> <br/> |
| <span data-ttu-id="638d0-114">[**CreateLayer (D2D1 \_ taille \_ F \* , ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="638d0-114">[**CreateLayer(D2D1\_SIZE\_F\*,ID2D1Layer\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))</span></span> | <span data-ttu-id="638d0-115">Crée une ressource de couche qui peut être utilisée avec cette cible de rendu et ses cibles de rendu compatibles.</span><span class="sxs-lookup"><span data-stu-id="638d0-115">Creates a layer resource that can be used with this render target and its compatible render targets.</span></span> <span data-ttu-id="638d0-116">La nouvelle couche a la taille initiale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="638d0-116">The new layer has the specified initial size.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="638d0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="638d0-117">Remarks</span></span>

<span data-ttu-id="638d0-118">La couche se redimensionne automatiquement, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="638d0-118">The layer automatically resizes itself, as needed.</span></span>

## <a name="examples"></a><span data-ttu-id="638d0-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="638d0-119">Examples</span></span>

<span data-ttu-id="638d0-120">L’exemple suivant utilise une couche pour découper une image bitmap en un masque géométrique.</span><span class="sxs-lookup"><span data-stu-id="638d0-120">The following example uses a layer to clip a bitmap to a geometric mask.</span></span> <span data-ttu-id="638d0-121">Pour obtenir un exemple complet, consultez [Comment découper un masque géométrique](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="638d0-121">For the complete example, see [How to Clip to a Geometric Mask](how-to-clip-with-layers.md).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="638d0-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="638d0-122">Requirements</span></span>



| <span data-ttu-id="638d0-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="638d0-123">Requirement</span></span> | <span data-ttu-id="638d0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="638d0-124">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="638d0-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="638d0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="638d0-126"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="638d0-126"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="638d0-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="638d0-127">Library</span></span><br/> | <dl> <span data-ttu-id="638d0-128"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="638d0-128"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="638d0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="638d0-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="638d0-130"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="638d0-130"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="638d0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="638d0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="638d0-132">Vue d’ensemble des couches</span><span class="sxs-lookup"><span data-stu-id="638d0-132">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> <dt>

[<span data-ttu-id="638d0-133">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="638d0-133">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

<span data-ttu-id="638d0-134">�</span><span class="sxs-lookup"><span data-stu-id="638d0-134">�</span></span>

<span data-ttu-id="638d0-135">�</span><span class="sxs-lookup"><span data-stu-id="638d0-135">�</span></span>
