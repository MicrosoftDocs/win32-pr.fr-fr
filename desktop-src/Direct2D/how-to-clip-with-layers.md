---
title: Comment découper un masque géométrique
description: Montre comment découper une région avec des couches.
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 979281fb7fa6e034894bffaecbd6246fe8a9aa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463450"
---
# <a name="how-to-clip-to-a-geometric-mask"></a><span data-ttu-id="68f19-103">Comment découper un masque géométrique</span><span class="sxs-lookup"><span data-stu-id="68f19-103">How to Clip to a Geometric Mask</span></span>

<span data-ttu-id="68f19-104">Cette rubrique explique comment utiliser un masque géométrique pour découper une région d’une couche.</span><span class="sxs-lookup"><span data-stu-id="68f19-104">This topic describes how to use a geometric mask to clip a region of a layer.</span></span>

<span data-ttu-id="68f19-105">**Pour découper une région avec un masque géométrique**</span><span class="sxs-lookup"><span data-stu-id="68f19-105">**To clip a region with a geometric mask**</span></span>

1.  <span data-ttu-id="68f19-106">Créez le [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) qui sera utilisé pour découper la région.</span><span class="sxs-lookup"><span data-stu-id="68f19-106">Create the [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) that will be used to clip the region.</span></span>
2.  <span data-ttu-id="68f19-107">Appelez [**ID2D1RenderTarget :: CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) pour créer une couche.</span><span class="sxs-lookup"><span data-stu-id="68f19-107">Call [**ID2D1RenderTarget::CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>
3.  <span data-ttu-id="68f19-108">Appelez [**ID2D1RenderTarget ::P ushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) et transmettez le masque géométrique que vous avez défini à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="68f19-108">Call [**ID2D1RenderTarget::PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and pass the geometric mask you defined in step 1.</span></span>
4.  <span data-ttu-id="68f19-109">Dessinez le contenu à découper.</span><span class="sxs-lookup"><span data-stu-id="68f19-109">Draw the content to clip.</span></span>
5.  <span data-ttu-id="68f19-110">Appelez [**ID2D1RenderTarget ::P OPlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) pour supprimer la couche de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="68f19-110">Call [**ID2D1RenderTarget::PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to remove the layer from the render target.</span></span>

<span data-ttu-id="68f19-111">L’exemple qui suit utilise un masque géométrique pour découper une image et plusieurs rectangles.</span><span class="sxs-lookup"><span data-stu-id="68f19-111">The example that follows uses a geometric mask to clip an image and several rectangles.</span></span> <span data-ttu-id="68f19-112">L’illustration suivante montre l’image bitmap d’origine sur la gauche et la bitmap découpée vers le masque géométrique situé à droite.</span><span class="sxs-lookup"><span data-stu-id="68f19-112">The following illustration shows the original bitmap on the left, and the bitmap clipped to the geometric mask on the right.</span></span>

![illustration d’une image bitmap Goldfish avant et après le découpage de la bitmap en un masque en forme d’étoile](images/cliparegion-layers.png)

<span data-ttu-id="68f19-114">Pour découper le dessin comme indiqué dans l’illustration précédente, vous créez un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) et vous l’utilisez pour définir une étoile.</span><span class="sxs-lookup"><span data-stu-id="68f19-114">To clip the drawing as shown in the preceding illustration, you create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and use it to define a star.</span></span> <span data-ttu-id="68f19-115">Le code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="68f19-115">The following code shows how to do this.</span></span>


```C++
// Create the path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
}

// Write to the path geometry using the geometry sink to create a star.
if (SUCCEEDED(hr))
{
    hr = m_pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
    pSink->BeginFigure(D2D1::Point2F(20, 50), D2D1_FIGURE_BEGIN_FILLED);
    pSink->AddLine(D2D1::Point2F(130, 50));
    pSink->AddLine(D2D1::Point2F(20, 130));
    pSink->AddLine(D2D1::Point2F(80, 0));
    pSink->AddLine(D2D1::Point2F(130, 130));
    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}

SafeRelease(&pSink);
```



<span data-ttu-id="68f19-116">Appelez [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) pour créer une couche.</span><span class="sxs-lookup"><span data-stu-id="68f19-116">Call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>

> [!Note]  
> <span data-ttu-id="68f19-117">À compter de Windows 8, vous n’avez pas besoin d’appeler [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)).</span><span class="sxs-lookup"><span data-stu-id="68f19-117">Starting with Windows 8, you don't need to call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)).</span></span> <span data-ttu-id="68f19-118">Dans la plupart des cas, les performances sont meilleures si vous n’appelez pas cette méthode et que Direct2D gère les ressources de couche.</span><span class="sxs-lookup"><span data-stu-id="68f19-118">In most situations performance is better if you don't call this method and Direct2D manages the layer resources.</span></span>

 

<span data-ttu-id="68f19-119">Appelez [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) avec le masque Geometry pour pousser la couche.</span><span class="sxs-lookup"><span data-stu-id="68f19-119">Call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) with the geometry mask to push the layer.</span></span> <span data-ttu-id="68f19-120">Dessinez le contenu sur clip, puis appelez [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) pour dépiler la couche.</span><span class="sxs-lookup"><span data-stu-id="68f19-120">Draw the content to clip, then call [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to pop the layer.</span></span> <span data-ttu-id="68f19-121">Cela produit le dessin en forme d’étoile.</span><span class="sxs-lookup"><span data-stu-id="68f19-121">This produces the star-shaped drawing.</span></span> <span data-ttu-id="68f19-122">Le code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="68f19-122">The following code shows how to do this.</span></span>


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

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

    SafeRelease(&pLayer);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="68f19-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68f19-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68f19-124">Vue d’ensemble des couches</span><span class="sxs-lookup"><span data-stu-id="68f19-124">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> <dt>

[<span data-ttu-id="68f19-125">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="68f19-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 