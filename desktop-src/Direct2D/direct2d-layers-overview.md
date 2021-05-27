---
title: Vue d’ensemble des couches
description: Décrit les principes de base des couches Direct2D.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, couches
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: ac68ba25d1e8f35c5a41daec4d7a5295235a5d98
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549184"
---
# <a name="layers-overview"></a>Vue d’ensemble des couches

Cette vue d’ensemble décrit les principes fondamentaux de l’utilisation des couches Direct2D. Elle contient les sections suivantes.

-   [Que sont les couches ?](#what-are-layers)
-   [Couches dans Windows 8 et versions ultérieures](#layers-in-windows-8-and-later)
    -   [ID2D1DeviceContext et PushLayer](#id2d1devicecontext-and-pushlayer)
    -   [Couche \_ d2d1 \_ PARAMETERS1 et d2d1 \_ couche \_ options1](/windows)
    -   [Modes de fusion](#blend-modes)
    -   [Interopérabilité](#interoperation)
-   [Créer des couches](#creating-layers)
-   [Limites du contenu](#content-bounds)
-   [Masques géométriques](#geometric-masks)
-   [Masques d’opacité](#opacity-masks)
-   [Alternatives aux couches](#alternatives-to-layers)
-   [Découpage d’une forme arbitraire](#clipping-an-arbitrary-shape)
    -   [Clips alignés sur l’axe](#axis-aligned-clips)
-   [Rubriques connexes](#related-topics)

## <a name="what-are-layers"></a>Que sont les couches ?

Les couches, représentées par les objets [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , permettent à une application de manipuler un groupe d’opérations de dessin. Vous utilisez une couche en la « poussant » sur une cible de rendu. Les opérations de dessin ultérieures effectuées par la cible de rendu sont dirigées vers la couche. Une fois que vous avez terminé avec la couche, vous « pop » la couche à partir de la cible de rendu, qui répartit le contenu de la couche sur la cible de rendu.

Comme les pinceaux, les couches sont des ressources dépendantes du périphérique créées par des cibles de rendu. Les couches peuvent être utilisées sur n’importe quelle cible de rendu dans le même domaine de ressource qui contient la cible de rendu qui l’a créée. Toutefois, une ressource de couche ne peut être utilisée que par une cible de rendu à la fois. Pour plus d’informations sur les ressources, consultez [vue d’ensemble des ressources](resources-and-resource-domains.md).

Bien que les couches offrent une technique de rendu puissante pour produire des effets intéressants, un nombre excessif de couches dans une application peut nuire à ses performances, en raison des différents coûts associés à la gestion des couches et des ressources de couche. Par exemple, il y a un coût de remplissage ou d’effacement de la couche, puis de la fusionner de nouveau, en particulier sur du matériel de haut de gamme. Ensuite, il y a le coût de la gestion des ressources de couche. Si vous les réallouez fréquemment, les blocages résultants sur le GPU sont le problème le plus significatif. Lorsque vous concevez votre application, essayez d’optimiser la réutilisation des ressources de couche.

## <a name="layers-in-windows-8-and-later"></a>Couches dans Windows 8 et versions ultérieures

Windows 8 a introduit de nouvelles API liées à la couche qui simplifient, améliorent les performances de et ajoutent des fonctionnalités aux couches.

### <a name="id2d1devicecontext-and-pushlayer"></a>ID2D1DeviceContext et PushLayer

L’interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) est dérivée de l’interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) et est la clé de l’affichage du contenu Direct2D dans Windows 8. pour plus d’informations sur cette interface, consultez [contextes de périphériques et](devices-and-device-contexts.md)de périphériques. Avec l’interface de contexte de périphérique, vous pouvez ignorer l’appel de la méthode [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , puis passer la valeur null à la méthode [**ID2D1DeviceContext ::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) . Direct2D gère automatiquement la ressource de couche et peut partager des ressources entre les couches et les graphiques d’effet.

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a>Couche \_ d2d1 \_ PARAMETERS1 et d2d1 \_ couche \_ options1

La [**structure \_ \_ PARAMETERS1 de la couche d2d1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) est la même que celle des [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), sauf que le membre final de la structure est maintenant une énumération options1 de la [**\_ couche \_ d2d1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) .

[**D2d1 \_ La couche \_ options1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) n’a pas d’option ClearType et a deux options différentes que vous pouvez utiliser pour améliorer les performances :

-   [**D2d1 \_ \_Initialisation de la couche options1 \_ \_ à partir de l' \_ arrière-plan**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D effectue le rendu des primitives sur la couche sans l’effacer avec le noir transparent. Il ne s’agit pas de la valeur par défaut, mais dans la plupart des cas, il en résulte une amélioration des performances.

-   [**D2d1 \_ Options1 de la couche \_ \_ Ignorer \_ alpha**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): si la surface sous-jacente est définie sur [**d2d1 \_ \_ mode Alpha \_ ignorée**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), cette option permet à Direct2D d’éviter de modifier le canal alpha de la couche. Ne l’utilisez pas dans d’autres cas.

### <a name="blend-modes"></a>Modes de fusion

À compter de Windows 8, le contexte de périphérique a un [**mode de fusion primitif**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) qui détermine la façon dont chaque primitive est fusionnée avec la surface cible. Ce mode s’applique également aux couches lorsque vous appelez la méthode [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .

Par exemple, si vous utilisez une couche pour découper des primitives avec transparence, définissez le mode de [**\_ \_ \_ copie de fusion primitif d2d1**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) sur le contexte de périphérique pour obtenir des résultats corrects. Le mode de copie fait en sorte que le contexte de l’appareil effectue l’interpolation linéaire sur les 4 canaux de couleur, y compris le canal alpha, de chaque pixel avec le contenu de la surface cible en fonction du masque géométrique de la couche.

### <a name="interoperation"></a>Interopérabilité

À partir de Windows 8, Direct2D prend en charge l’interopérabilité avec Direct3D et GDI lorsqu’une couche ou un clip est poussé. Vous appelez [**ID2D1GdiInteropRenderTarget :: GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) alors qu’une couche est Poussée pour interagir avec GDI. Vous appelez [**ID2D1DeviceContext :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) , puis le rendu sur la surface sous-jacente pour interagir avec Direct3D. Il est de votre responsabilité d’effectuer un rendu à l’intérieur de la couche ou du clip avec Direct3D ou GDI. Si vous essayez d’effectuer un rendu à l’extérieur de la couche ou de découper, les résultats ne sont pas définis.

## <a name="creating-layers"></a>Créer des couches

L’utilisation de couches nécessite une bonne connaissance des méthodes [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))et [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , ainsi que de la structure des paramètres de la [**\_ \_ couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) , qui contient un ensemble de données paramétriques qui définissent la façon dont la couche peut être utilisée. La liste suivante décrit les méthodes et la structure.

-   Appelez la méthode [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) pour créer une ressource de couche.
    > [!Note]  
    > À partir de Windows 8, vous pouvez ignorer l’appel de la méthode [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , puis passer NULL à la méthode [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) sur l’interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) . C’est plus simple et permet à Direct2D de gérer automatiquement la ressource de couche et de partager les ressources entre les couches et les graphiques d’effet.

     

-   Une fois que la cible de rendu a commencé le dessin (une fois que sa méthode [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) a été appelée), vous pouvez utiliser la méthode [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) . La méthode **PushLayer** ajoute la couche spécifiée à la cible de rendu, afin que la cible reçoive toutes les opérations de dessin suivantes jusqu’à ce que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) soit appelé. Cette méthode prend un objet [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) retourné en appelant [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) et un *layerParameters* dans la structure des [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) . Le tableau suivant décrit les champs de la structure. 

    | Champ                 | Description|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **contentBounds**     | Limites de contenu de la couche. Le contenu en dehors de ces limites est garanti qu’il n’est pas rendu. La valeur par défaut de ce paramètre est [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect). Lorsque la valeur par défaut est utilisée, les limites de contenu sont effectivement prises pour être les limites de la cible de rendu. |
    | **geometricMask**     | Facultatif Zone, définie par un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), à laquelle la couche doit être découpée. A la valeur **null** si la couche ne doit pas être découpée en géométrie. |
    | **maskAntialiasMode** | Valeur qui spécifie le mode d’anticrénelage pour le masque géométrique spécifié par le champ **geometricMask** . |
    | **maskTransform**     | Valeur qui spécifie la transformation appliquée au masque géométrique lors de la composition de la couche. Cela est relatif à la transformation universelle.  |
    | **'**           | Valeur d’opacité de la couche. L’opacité de chaque ressource de la couche est multipliée par cette valeur lors de la composition vers la cible.  |
    | **opacityBrush**      | Facultatif Pinceau utilisé pour modifier l’opacité de la couche. Le pinceau est mappé à la couche et le canal alpha de chaque pixel de pinceau mappé est multiplié par rapport au pixel de couche correspondant. Affectez la valeur **null** si la couche ne doit pas avoir de masque d’opacité.   |
    | **layerOptions**      | Valeur qui spécifie si la couche envisage de restituer du texte avec l’anticrénelage ClearType. Par défaut, ce paramètre a la valeur OFF. Son activation permet à ClearType de fonctionner correctement, mais cela entraîne une vitesse de rendu légèrement plus lente.    |

    

     

    > [!Note]  
    > À partir de Windows 8, vous ne pouvez pas effectuer de rendu avec ClearType dans une couche, donc le paramètre **layerOptions** doit toujours être défini sur [**options de \_ couche d2d1 \_ \_ aucune**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)

     

    Pour plus de commodité, Direct2D fournit la méthode [**d2d1 :: LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) pour vous aider à créer des structures de [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .

-   Pour compositiser le contenu de la couche dans la cible de rendu, appelez la méthode [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) . Vous devez appeler la méthode **PopLayer** avant d’appeler la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .

L’exemple suivant montre comment utiliser [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))et [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer). Tous les champs de la structure des [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) sont définis sur leurs valeurs par défaut, à l’exception de **opacityBrush**, qui est défini sur un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).


```C++
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
```



Le code a été omis de cet exemple.

Notez que lorsque vous appelez [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) et [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), vérifiez que chaque **PushLayer** a un appel **PopLayer** correspondant. S’il y a plus d’appels **PopLayer** que d’appels **PushLayer** , la cible de rendu est placée dans un état d’erreur. Si [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) est appelé avant que toutes les couches en suspens soient dépilées, la cible de rendu est placée dans un état d’erreur et retourne une erreur. Pour effacer l’état d’erreur, utilisez [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="content-bounds"></a>Limites du contenu

**ContentBounds** définit la limite de ce qui doit être dessiné sur la couche. Seuls les éléments des limites de contenu sont composites à la cible de rendu.

L’exemple suivant montre comment spécifier **contentBounds** afin que l’image d’origine soit découpée en limites de contenu avec l’angle supérieur gauche à (10, 108) et le coin inférieur droit à (121, 177). L’illustration suivante montre l’image d’origine et le résultat du découpage de l’image vers les limites du contenu.

![illustration de limites de contenu sur une image d’origine et l’image découpée résultante](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



Le code a été omis de cet exemple.

> [!Note]
>
> L’image découpée résultante est également affectée si vous spécifiez un **geometricMask**. Pour plus d’informations, consultez la section [masques géométriques](#geometric-masks) .

 

## <a name="geometric-masks"></a>Masques géométriques

Un masque géométrique est un élément ou un découpage, défini par un objet [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , qui masque une couche lorsqu’elle est dessinée par une cible de rendu. Vous pouvez utiliser le champ **geometricMask** de la structure des [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) pour masquer les résultats dans une géométrie. Par exemple, si vous souhaitez afficher une image masquée par une lettre de bloc « A », vous pouvez d’abord créer une géométrie représentant la lettre « A » et utiliser cette géométrie comme masque géométrique pour une couche. Ensuite, après avoir effectué un push de la couche, vous pouvez dessiner l’image. Le fait de détourer la couche entraîne le découpage de l’image en forme de lettre « A ».

L’exemple suivant montre comment créer un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) contenant une forme de montagne, puis passer la géométrie du tracé à [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)). Il dessine ensuite une bitmap et des carrés. S’il n’existe qu’une image bitmap à afficher dans la couche, utilisez [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) avec un pinceau bitmap avec pincement pour plus d’efficacité. L’illustration suivante montre la sortie de l’exemple.

![illustration d’une image d’une feuille et de l’image résultante après l’application d’un masque géométrique d’une montagne](images/layers-bitmapmask.png)

Le premier exemple définit la géométrie à utiliser comme masque.


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



L’exemple suivant utilise la géométrie comme masque pour la couche.


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

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



Le code a été omis de cet exemple.

> [!Note]
>
> En général, si vous spécifiez un **geometricMask**, vous pouvez utiliser la valeur par défaut, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), pour **contentBounds**.
>
> Si **contentBounds** a la valeur null et que **GEOMETRICMASK** est non null, les limites de contenu sont en fait les limites du masque géométrique après l’application de la transformation de masque.
>
> Si **contentBounds** n’a pas la valeur null et que **geometricMask** n’a pas la valeur null, le masque géométrique transformé est correctement rogné par rapport aux limites de contenu et les limites de contenu sont supposées être infinies.

 

## <a name="opacity-masks"></a>Masques d’opacité

Un masque d’opacité est un masque, décrit par un pinceau ou un bitmap, qui est appliqué à un autre objet pour rendre cet objet partiellement ou complètement transparent. Il permet d’utiliser le canal alpha d’un pinceau à utiliser comme masque de contenu. Par exemple, vous pouvez définir un pinceau de dégradé radial qui varie d’opaque à transparent pour créer un effet d’vignette.

L’exemple qui suit utilise un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) comme masque d’opacité. Il dessine ensuite une bitmap et des carrés. S’il n’existe qu’une image bitmap à afficher dans la couche, utilisez [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) avec un pinceau bitmap avec pincement pour plus d’efficacité. L’illustration suivante montre la sortie de cet exemple.

![illustration d’une image d’arbres et de l’image résultante après l’application d’un masque d’opacité](images/layers-opacitymask.png)


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



Le code a été omis de cet exemple.

> [!Note]  
> Cet exemple utilise une couche pour appliquer un masque d’opacité à un objet unique pour que l’exemple reste aussi simple que possible. Lors de l’application d’un masque d’opacité à un objet unique, il est plus efficace d’utiliser les méthodes [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) ou [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , plutôt qu’une couche.

 

Pour obtenir des instructions sur l’application d’un masque d’opacité sans utiliser de couche, consultez [vue d’ensemble des masques d’opacité](opacity-masks-overview.md).

## <a name="alternatives-to-layers"></a>Alternatives aux couches

Comme mentionné précédemment, un nombre excessif de couches peut nuire aux performances de votre application. Pour améliorer les performances, évitez d’utiliser les couches dans la mesure du possible ; Utilisez plutôt leurs alternatives. L’exemple de code suivant montre comment utiliser [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) et [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pour découper une région, comme alternative à l’utilisation d’une couche avec des limites de contenu.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



De même, utilisez [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) avec un pinceau bitmap avec pincement, comme alternative à l’utilisation d’une couche avec un masque d’opacité lorsqu’il n’existe qu’un seul contenu à afficher dans la couche, comme illustré dans l’exemple suivant.


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



En guise d’alternative à l’utilisation d’une couche avec un masque géométrique, envisagez d’utiliser un masque bitmap pour découper une région, comme illustré dans l’exemple suivant.


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



Enfin, si vous souhaitez appliquer l’opacité à une seule primitive, vous devez multiplier l’opacité dans la couleur du pinceau, puis restituer la primitive. Vous n’avez pas besoin d’une image bitmap de masque d’opacité ou de couche.


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a>Découpage d’une forme arbitraire

La figure ci-dessous illustre le résultat de l’application d’un clip à une image.

![image qui montre un exemple d’image avant et après un clip.](images/clip.png)

Vous pouvez obtenir ce résultat en utilisant des couches avec un masque Geometry ou la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) avec un pinceau d’opacité.

Voici un exemple qui utilise une couche :


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Voici un exemple qui utilise la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



Dans cet exemple de code, lorsque vous appelez la méthode PushLayer, vous ne transmettez pas de couche créée par une application. Direct2D crée une couche pour vous. Direct2D est en mesure de gérer l’allocation et la destruction de cette ressource sans aucune implication de l’application. Cela permet à Direct2D de réutiliser des couches en interne et d’appliquer des optimisations de gestion des ressources.

> [!Note]  
> Dans Windows 8, de nombreuses optimisations ont été apportées à l’utilisation des couches et nous vous recommandons d’essayer d’utiliser les API de couche au lieu de [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) chaque fois que cela est possible.

 

### <a name="axis-aligned-clips"></a>Clips alignés sur l’axe

Si la région à découper est alignée sur l’axe de la surface de dessin, plutôt que arbitraire. Ce cas est adapté à l’utilisation d’un rectangle de découpage au lieu d’une couche. Le gain de performance est plus pour la géométrie avec alias que la géométrie avec anticrénelage. Pour plus d’informations sur les clips alignés sur l’axe, consultez la rubrique [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 