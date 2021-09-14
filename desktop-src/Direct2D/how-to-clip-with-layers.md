---
title: Comment découper un masque géométrique
description: Montre comment découper une région avec des couches.
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 979281fb7fa6e034894bffaecbd6246fe8a9aa94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113145"
---
# <a name="how-to-clip-to-a-geometric-mask"></a>Comment découper un masque géométrique

Cette rubrique explique comment utiliser un masque géométrique pour découper une région d’une couche.

**Pour découper une région avec un masque géométrique**

1.  Créez le [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) qui sera utilisé pour découper la région.
2.  Appelez [**ID2D1RenderTarget :: CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) pour créer une couche.
3.  Appelez [**ID2D1RenderTarget ::P ushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) et transmettez le masque géométrique que vous avez défini à l’étape 1.
4.  Dessinez le contenu à découper.
5.  Appelez [**ID2D1RenderTarget ::P OPlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) pour supprimer la couche de la cible de rendu.

L’exemple qui suit utilise un masque géométrique pour découper une image et plusieurs rectangles. L’illustration suivante montre l’image bitmap d’origine sur la gauche et la bitmap découpée vers le masque géométrique situé à droite.

![illustration d’une image bitmap Goldfish avant et après le découpage de la bitmap en un masque en forme d’étoile](images/cliparegion-layers.png)

Pour découper le dessin comme indiqué dans l’illustration précédente, vous créez un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) et vous l’utilisez pour définir une étoile. Le code suivant montre comment procéder.


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



Appelez [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) pour créer une couche.

> [!Note]  
> à partir de Windows 8, vous n’avez pas besoin d’appeler [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)). Dans la plupart des cas, les performances sont meilleures si vous n’appelez pas cette méthode et que Direct2D gère les ressources de couche.

 

Appelez [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) avec le masque Geometry pour pousser la couche. Dessinez le contenu sur clip, puis appelez [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) pour dépiler la couche. Cela produit le dessin en forme d’étoile. Le code suivant montre comment procéder.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des couches](direct2d-layers-overview.md)
</dt> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 