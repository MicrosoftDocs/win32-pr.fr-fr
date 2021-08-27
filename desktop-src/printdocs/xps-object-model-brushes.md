---
description: Cette rubrique explique comment utiliser différents types de pinceaux dans un modèle d’objet XPS.
ms.assetid: 392ca1d5-283e-4eed-ae21-6477c469014d
title: Pinceaux OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbca4174c406e0d2fda63d932ee85f2f3c3123b7255b43f77a2365bf0f05e2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971128"
---
# <a name="xps-om-brushes"></a>Pinceaux OM XPS

Cette rubrique explique comment utiliser différents types de pinceaux dans un modèle d’objet XPS.

Les pinceaux dans le modèle d’objet XPS sont basés sur l' [**interface IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) et incluent les éléments suivants :

<dl> Pinceaux de mosaïque

-   [**Interface IXpsOMTileBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
-   [**Interface IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
-   [**Interface IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
-   [**Interface IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)

  
Pinceaux de dégradé

-   [**Interface IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
-   [**Interface IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
-   [**Interface IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)

  
</dl>

## <a name="code-examples"></a>Exemples de code

### <a name="create-a-solid-color-brush"></a>Créer un pinceau de couleur unie

L’exemple de code suivant crée un pinceau de couleur unie à partir d’une valeur de couleur qui est définie dans le code.


```C++
    HRESULT                hr = S_OK;

    XPS_COLOR              xpsColor;
    IXpsOMSolidColorBrush  *brush;

    // creates a solid red brush
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush(
       &xpsColor, 
       NULL, 
       reinterpret_cast<IXpsOMSolidColorBrush**>(&brush));
    
    // use brush

    // when finished with brush, release pointer
    brush->Release();
```



### <a name="create-a-visual-brush"></a>Créer un pinceau visuel

L’exemple de code suivant crée un pinceau à partir d’un objet visuel.


```C++
    HRESULT                       hr = S_OK;
    IXpsOMVisualBrush             *brush;

    XPS_RECT viewBoxRect = {0,0,0,0};
    XPS_RECT viewPortRect = {0,0,0,0};

    // set viewBoxRect to define the portion of the visual to use
    // as the brush.
    //
    // set viewPortRect to define the location and size of the 
    // the brush in the destination 
    //
    // create the brush
    hr = xpsFactory->CreateVisualBrush (
        &viewBoxRect,
        &viewPortRect,
        reinterpret_cast<IXpsOMVisualBrush**>(&brush));

    // assign the visual object
    //   brushVisual points to a visual
    //   that is defined outside of this example

    hr = brush->SetVisualLocal (brushVisual);
    
    // use brush
    
    // when finished with brush, release pointer
    brush->Release();
    
```



### <a name="create-an-image-brush"></a>Créer un pinceau image

Reportez-vous à l’exemple de code dans [placer des images dans un modèle d’objet XPS](place-images-in-an-xps-om.md).

### <a name="create-a-linear-gradient-brush"></a>Créer un pinceau de dégradé linéaire

L’exemple de code suivant crée un pinceau de dégradé linéaire. Le dégradé a deux points de dégradé.


```C++
    HRESULT                       hr = S_OK;
    XPS_COLOR                     xpsColorStop;
    IXpsOMGradientStop            *xpsGradientStop1, *xpsGradientStop2;
    IXpsOMLinearGradientBrush     *brush;
    XPS_POINT                     startPoint, endPoint;

    // define the start color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xE4;
    xpsColorStop.value.sRGB.green = 0x3B;
    xpsColorStop.value.sRGB.blue  = 0x2F;
    
    // create a gradient stop by setting the color and location 
    // for the beginning of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop, 
        NULL, 
        0.0f,
        &xpsGradientStop1);
    startPoint.x = 375.75f;
    startPoint.y = 18.0f;

    // define the end color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xEF;
    xpsColorStop.value.sRGB.green = 0x79;
    xpsColorStop.value.sRGB.blue  = 0x2F;

    // create a gradient stop by setting the color and  location
    //  for the end of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop,
        NULL, 
        1.0f, 
        &xpsGradientStop2);
    endPoint.x   = 375.75f;
    endPoint.y   = 134.6f;

    // create the brush
    hr = xpsFactory->CreateLinearGradientBrush(
        xpsGradientStop1, 
        xpsGradientStop2, 
        &startPoint, 
        &endPoint, 
        &brush);
    // release gradient stops after creating brush
    xpsGradientStop1->Release();
    xpsGradientStop2->Release();

    // when finished with brush, release pointer to brush
    brush->Release();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
</dt> <dt>

[**Interface IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)
</dt> <dt>

[**Interface IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
</dt> <dt>

[**Interface IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)
</dt> <dt>

[**Interface IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[**Interface IXpsOMTileBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
</dt> <dt>

[**Interface IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
</dt> <dt>

[**\_couleur XPS**](xps-color.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



