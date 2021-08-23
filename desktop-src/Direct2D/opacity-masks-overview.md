---
title: Vue d'ensemble des masques d'opacité
description: Cette rubrique explique comment utiliser des bitmaps et des pinceaux pour définir des masques d’opacité. Elle contient les sections suivantes.
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51626fb2c76b82adeb3b12324db4652a62167db344f41e861c7b0f1d116059ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636308"
---
# <a name="opacity-masks-overview"></a>Vue d'ensemble des masques d'opacité

Cette rubrique explique comment utiliser des bitmaps et des pinceaux pour définir des masques d’opacité. Elle contient les sections suivantes.

-   [Composants requis](#prerequisites)
-   [Qu’est-ce qu’un masque d’opacité ?](#what-is-an-opacity-mask)
-   [Utiliser une image bitmap comme masque d’opacité avec la méthode FillOpacityMask](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [Utiliser un pinceau comme masque d’opacité avec la méthode FillGeometry](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [Utiliser un pinceau de dégradé linéaire comme masque d’opacité](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [Utiliser un pinceau de dégradé radial comme masque d’opacité](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [Appliquer un masque d’opacité à une couche](#apply-an-opacity-mask-to-a-layer)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Cette vue d’ensemble suppose que vous êtes familiarisé avec les opérations de dessin Direct2D de base, comme décrit dans la procédure pas à pas [création d’une application Direct2d simple](direct2d-quickstart.md) . Vous devez également être familiarisé avec les différents types de pinceaux, comme décrit dans la [vue d’ensemble des pinceaux](direct2d-brushes-overview.md).

## <a name="what-is-an-opacity-mask"></a>Qu’est-ce qu’un masque d’opacité ?

Un masque d’opacité est un masque, décrit par un pinceau ou un bitmap, qui est appliqué à un autre objet pour rendre cet objet partiellement ou complètement transparent. Un masque d’opacité utilise des informations de canal alpha pour spécifier la façon dont les pixels source de l’objet sont fusionnés dans la cible de destination finale. Les parties transparentes du masque indiquent les zones où l’image sous-jacente est masquée, tandis que les parties opaques du masque indiquent où l’objet masqué est visible.

Il existe plusieurs façons d’appliquer un masque d’opacité :

-   Utilisez la méthode [**ID2D1RenderTarget :: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) . La méthode **FillOpacityMask** peint une zone rectangulaire d’une cible de rendu, puis applique un masque d’opacité, défini par une image bitmap. Utilisez cette méthode lorsque votre masque d’opacité est un bitmap et que vous souhaitez remplir une zone rectangulaire.
-   Utilisez la méthode [**ID2D1RenderTarget :: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) . La méthode **FillGeometry** peint l’intérieur de Geometry avec le [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)spécifié, puis applique un masque d’opacité défini par un pinceau. Utilisez cette méthode lorsque vous souhaitez appliquer un masque d’opacité à une géométrie ou si vous souhaitez utiliser un pinceau comme masque d’opacité.
-   Utilisez un [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) pour appliquer un masque d’opacité. Utilisez cette approche lorsque vous souhaitez appliquer un masque d’opacité à un groupe de contenu de dessin, et pas simplement à une seule forme ou image. Pour plus d’informations, consultez [vue d’ensemble des couches](direct2d-layers-overview.md).

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a>Utiliser une image bitmap comme masque d’opacité avec la méthode FillOpacityMask

La méthode [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) peint une zone rectangulaire d’une cible de rendu, puis applique un masque d’opacité, défini par un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap). Utilisez cette méthode lorsque vous avez une bitmap que vous souhaitez utiliser comme masque d’opacité pour une zone rectangulaire.

Le diagramme suivant illustre l’application du masque d’opacité (un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) avec une image de fleur) à un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) avec l’image d’une usine de Palms. L’image résultante est une image bitmap d’une plante découpée en forme de fleur.

![diagramme d’une bitmap de fleur utilisée comme masque d’opacité sur une image d’une plante de Palm](images/brushes-ovw-bitmapopacity.png)

Les exemples de code suivants montrent comment procéder.

Le premier exemple charge la bitmap suivante, *m \_ pBitmapMask*, pour une utilisation en tant que masque bitmap. L’illustration suivante montre la sortie produite. Notez que, bien que la partie opaque de la bitmap apparaisse en noir, les informations de couleur de la bitmap n’ont aucun effet sur le masque d’opacité. seules les informations d’opacité de chaque pixel de la bitmap sont utilisées. Les pixels entièrement opaques de cette bitmap ont été colorés en noir à titre d’illustration uniquement.

![illustration du masque de bitmap de fleur](images/bitmapmask.png)

Dans cet exemple, le [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) est chargé par une méthode d’assistance, LoadResourceBitmap, définie ailleurs dans l’exemple.


```C++
            if (SUCCEEDED(hr))
            {
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"BitmapMask",
                    L"Image",
                    &m_pBitmapMask
                    );
            }
```



L’exemple suivant définit le pinceau, *m \_ pFernBitmapBrush*, auquel le masque d’opacité est appliqué. Cet exemple utilise un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) qui contient une image de Palm, mais vous pouvez utiliser à la place un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)ou [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) . L’illustration suivante montre la sortie produite.

![illustration de la bitmap utilisée par le pinceau bitmap](images/fern.png)


```C++
            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
                hr = m_pRenderTarget->CreateBitmapBrush(
                    m_pFernBitmap,
                    propertiesXClampYClamp,
                    &m_pFernBitmapBrush
                    );


            }
```





Maintenant que le masque d’opacité et le pinceau sont définis, vous pouvez utiliser la méthode [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) dans la méthode de rendu de votre application. Quand vous appelez la méthode **FillOpacityMask** , vous devez spécifier le type de masque d’opacité que vous utilisez : les **graphiques de contenu de masque d’opacité d2d1, les \_ \_ \_ \_ graphiques** de contenu de masque d’opacité **d2d1 de \_ \_ \_ \_ texte \_ naturel** et le **texte du contenu de masque d' \_ opacité d2d1 \_ \_ \_ \_ \_ compatible GDI**. Pour connaître la signification de ces trois types, consultez [**\_ contenu du \_ masque \_ d’opacité d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).

> [!Note]  
> à partir de Windows 8, [**le \_ \_ \_ contenu du masque d’opacité D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) n’est pas requis. Consultez la méthode [**ID2D1DeviceContext :: FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) , qui n’a aucun paramètre de **contenu de \_ \_ masque \_ d’opacité d2d1** .

 

L’exemple suivant définit le mode d’anticrénelage de la cible de rendu sur [**d2d1 \_ mode \_ anticrénelage \_ Aliased**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) afin que le masque d’opacité fonctionne correctement. Elle appelle ensuite la méthode [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) et la transmet au masque d’opacité (*m \_ pBitmapMask*), au pinceau auquel le masque d’opacité est appliqué (*m \_ pFernBitmapBrush*), au type de contenu à l’intérieur du masque d’opacité ([**\_ \_ \_ \_ graphiques de contenu du masque d’opacité d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) et à la zone à peindre. L’illustration suivante montre la sortie produite.

![illustration de l’image de la plante de Palm avec un masque d’opacité appliqué](images/opacitymaskoutput.png)


```C++
        D2D1_RECT_F rcBrushRect = D2D1::RectF(5, 5, 155, 155);


        // D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask to function properly
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);
        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);
```





Le code a été omis de cet exemple.

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a>Utiliser un pinceau comme masque d’opacité avec la méthode FillGeometry

La section précédente a décrit comment utiliser un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) comme masque d’opacité. Direct2D fournit également la méthode [**ID2D1RenderTarget :: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , qui vous permet de spécifier éventuellement Brush comme masque d’opacité quand vous remplissez un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry). Cela vous permet de créer des masques d’opacité à partir de dégradés (à l’aide de [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) ou [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) et de bitmaps (à l’aide de **ID2D1Bitmap**).

La méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) accepte trois paramètres :

-   Le premier paramètre, [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), définit la forme à peindre.
-   Le deuxième paramètre, [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), spécifie le pinceau utilisé pour peindre la géométrie. Ce paramètre doit être un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) dont les modes x et y sont définis sur le mode d' [**extension \_ d2d1 \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).
-   Le troisième paramètre, [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), spécifie un pinceau à utiliser comme masque d’opacité. Ce pinceau peut être [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)ou [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). (Techniquement, vous pouvez utiliser un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), mais l’utilisation d’un pinceau de couleur unie comme masque d’opacité ne produit pas de résultats intéressants.)

Les sections suivantes décrivent comment utiliser les objets [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) et [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) en tant que masques d’opacité.

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a>Utiliser un pinceau de dégradé linéaire comme masque d’opacité

Le diagramme suivant illustre l’effet de l’application d’un pinceau de dégradé linéaire à un rectangle rempli d’une image bitmap de fleurs.

![diagramme d’une image bitmap de fleur avec un pinceau dégradé linéaire appliqué](images/brushes-ovw-lineargradient-opacitymask.png)

Les étapes qui suivent décrivent comment recréer cet effet.

1.  Définissez le contenu à masquer. L’exemple suivant crée un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pLinearFadeFlowersBitmap*. Le mode étendu x et y-pour *m \_ pLinearFadeFlowersBitmap* sont définis sur le [**\_ mode d' \_ extension \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) pour qu’il puisse être utilisé avec un masque d’opacité par la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .

    ```cpp
    if (SUCCEEDED(hr))
    {
        // Create the bitmap to be used by the bitmap brush.
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"LinearFadeFlowers",
            L"Image",
            &m_pLinearFadeFlowersBitmap
            );
    }
 
    if (SUCCEEDED(hr))
        {
            D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                D2D1::BitmapBrushProperties(
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                );
    ```

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>C++</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>                if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateBitmapBrush(
                            m_pLinearFadeFlowersBitmap,
                            propertiesXClampYClamp,
                            &m_pLinearFadeFlowersBitmapBrush
                            );
                    }</code></pre></td>
    </tr>
    </tbody>
    </table>

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>C++</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  Définissez le masque d’opacité. L’exemple de code suivant crée un pinceau dégradé linéaire Diagonal (*m \_ pLinearGradientBrush*) qui apparaît en fondu du noir entièrement opaque à la position 0 au blanc complètement transparent à la position 1.
```C++
                if (SUCCEEDED(hr))
                {
                    ID2D1GradientStopCollection *pGradientStops = NULL;

                    static const D2D1_GRADIENT_STOP gradientStops[] =
                    {
                        {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                        {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                    };

                    hr = m_pRenderTarget->CreateGradientStopCollection(
                        gradientStops,
                        2,
                        &pGradientStops);


                    if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateLinearGradientBrush(
                            D2D1::LinearGradientBrushProperties(
                                D2D1::Point2F(0, 0),
                                D2D1::Point2F(150, 150)),
                            pGradientStops,
                            &m_pLinearGradientBrush);
                    }

    
                pGradientStops->Release();
                }
```



    

3.  Utilisez la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) . L’exemple final utilise la méthode **FillGeometry** dans le pinceau de contenu pour remplir [**un ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) avec un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pLinearFadeFlowersBitmap*) et applique un masque d’opacité (*m \_ pLinearGradientBrush*).
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

Le code a été omis de cet exemple.

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a>Utiliser un pinceau de dégradé radial comme masque d’opacité

Le diagramme suivant illustre l’effet visuel de l’application d’un pinceau de dégradé radial à un rectangle rempli avec une bitmap de feuillage.

![diagramme d’une bitmap de feuillage avec un pinceau de dégradé radial appliqué](images/brushes-ovw-radialgradient-opacitymask.png)

Le premier exemple crée un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pRadialFadeFlowersBitmapBrush*. Pour qu’il puisse être utilisé avec un masque d’opacité par la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , le mode d’extension x et y-pour *m \_ pRadialFadeFlowersBitmapBrush* sont définis sur le mode d' [**extension d2d1 \_ \_ \_ clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).


```C++
            if (SUCCEEDED(hr))
            {
                // Create the bitmap to be used by the bitmap brush.
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"RadialFadeFlowers",
                    L"Image",
                    &m_pRadialFadeFlowersBitmap
                    );
            }


            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateBitmapBrush(
                        m_pLinearFadeFlowersBitmap,
                        propertiesXClampYClamp,
                        &m_pLinearFadeFlowersBitmapBrush
                        );
                }</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



L’exemple suivant définit le pinceau de dégradé radial qui sera utilisé comme masque d’opacité.


```C++
            if (SUCCEEDED(hr))
            {
                ID2D1GradientStopCollection *pGradientStops = NULL;

                static const D2D1_GRADIENT_STOP gradientStops[] =
                {
                    {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                    {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                };

                hr = m_pRenderTarget->CreateGradientStopCollection(
                    gradientStops,
                    2,
                    &pGradientStops);




                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateRadialGradientBrush(
                        D2D1::RadialGradientBrushProperties(
                            D2D1::Point2F(75, 75),
                            D2D1::Point2F(0, 0),
                            75,
                            75),
                        pGradientStops,
                        &m_pRadialGradientBrush);
                }
                pGradientStops->Release();
            }
```





L’exemple de code final utilise [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pRadialFadeFlowersBitmapBrush*) et le masque d’opacité (*m \_ pRadialGradientBrush*) pour remplir un [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*).


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



Le code a été omis de cet exemple.

## <a name="apply-an-opacity-mask-to-a-layer"></a>Appliquer un masque d’opacité à une couche

Quand vous appelez [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) pour pousser un [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) sur une cible de rendu, vous pouvez utiliser la structure des [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) pour appliquer un pinceau comme masque d’opacité. L’exemple de code suivant utilise un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) comme masque d’opacité.


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



Pour plus d’informations sur l’utilisation des couches, consultez [vue d’ensemble des couches](direct2d-layers-overview.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des pinceaux](direct2d-brushes-overview.md)
</dt> <dt>

[Vue d’ensemble des couches](direct2d-layers-overview.md)
</dt> </dl>

 

 