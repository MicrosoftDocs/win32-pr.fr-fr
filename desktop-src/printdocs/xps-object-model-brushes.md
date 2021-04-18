---
description: Cette rubrique explique comment utiliser différents types de pinceaux dans un modèle d’objet XPS.
ms.assetid: 392ca1d5-283e-4eed-ae21-6477c469014d
title: Pinceaux OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0557757bfaf81156b2015525d35897cfb042e44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533820"
---
# <a name="xps-om-brushes"></a><span data-ttu-id="69cb5-103">Pinceaux OM XPS</span><span class="sxs-lookup"><span data-stu-id="69cb5-103">XPS OM Brushes</span></span>

<span data-ttu-id="69cb5-104">Cette rubrique explique comment utiliser différents types de pinceaux dans un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="69cb5-104">This topic describes how to use different types of brushes in an XPS OM.</span></span>

<span data-ttu-id="69cb5-105">Les pinceaux dans le modèle d’objet XPS sont basés sur l' [**interface IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) et incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="69cb5-105">The brushes in the XPS OM are based on the [**IXpsOMBrush Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) and include the following:</span></span>

<dl> <span data-ttu-id="69cb5-106">Pinceaux de mosaïque</span><span class="sxs-lookup"><span data-stu-id="69cb5-106">Tile Brushes</span></span>

-   [<span data-ttu-id="69cb5-107">**Interface IXpsOMTileBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-107">**IXpsOMTileBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
-   [<span data-ttu-id="69cb5-108">**Interface IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-108">**IXpsOMSolidColorBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
-   [<span data-ttu-id="69cb5-109">**Interface IXpsOMVisualBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-109">**IXpsOMVisualBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
-   [<span data-ttu-id="69cb5-110">**Interface IXpsOMImageBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-110">**IXpsOMImageBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)

  
<span data-ttu-id="69cb5-111">Pinceaux de dégradé</span><span class="sxs-lookup"><span data-stu-id="69cb5-111">Gradient Brushes</span></span>

-   [<span data-ttu-id="69cb5-112">**Interface IXpsOMGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-112">**IXpsOMGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
-   [<span data-ttu-id="69cb5-113">**Interface IXpsOMLinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-113">**IXpsOMLinearGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
-   [<span data-ttu-id="69cb5-114">**Interface IXpsOMRadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-114">**IXpsOMRadialGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)

  
</dl>

## <a name="code-examples"></a><span data-ttu-id="69cb5-115">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="69cb5-115">Code Examples</span></span>

### <a name="create-a-solid-color-brush"></a><span data-ttu-id="69cb5-116">Créer un pinceau de couleur unie</span><span class="sxs-lookup"><span data-stu-id="69cb5-116">Create a solid-color brush</span></span>

<span data-ttu-id="69cb5-117">L’exemple de code suivant crée un pinceau de couleur unie à partir d’une valeur de couleur qui est définie dans le code.</span><span class="sxs-lookup"><span data-stu-id="69cb5-117">The following code example creates a solid-color brush from a color value that is defined in the code.</span></span>


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



### <a name="create-a-visual-brush"></a><span data-ttu-id="69cb5-118">Créer un pinceau visuel</span><span class="sxs-lookup"><span data-stu-id="69cb5-118">Create a visual brush</span></span>

<span data-ttu-id="69cb5-119">L’exemple de code suivant crée un pinceau à partir d’un objet visuel.</span><span class="sxs-lookup"><span data-stu-id="69cb5-119">The following code example creates a brush from a visual object.</span></span>


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



### <a name="create-an-image-brush"></a><span data-ttu-id="69cb5-120">Créer un pinceau image</span><span class="sxs-lookup"><span data-stu-id="69cb5-120">Create an image brush</span></span>

<span data-ttu-id="69cb5-121">Reportez-vous à l’exemple de code dans [placer des images dans un modèle d’objet XPS](place-images-in-an-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="69cb5-121">Refer to the code example in [Place Images in an XPS OM](place-images-in-an-xps-om.md).</span></span>

### <a name="create-a-linear-gradient-brush"></a><span data-ttu-id="69cb5-122">Créer un pinceau de dégradé linéaire</span><span class="sxs-lookup"><span data-stu-id="69cb5-122">Create a linear-gradient brush</span></span>

<span data-ttu-id="69cb5-123">L’exemple de code suivant crée un pinceau de dégradé linéaire.</span><span class="sxs-lookup"><span data-stu-id="69cb5-123">The following code example creates a linear-gradient brush.</span></span> <span data-ttu-id="69cb5-124">Le dégradé a deux points de dégradé.</span><span class="sxs-lookup"><span data-stu-id="69cb5-124">The gradient has two gradient stops.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="69cb5-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69cb5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69cb5-126">**Interface IXpsOMGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-126">**IXpsOMGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
</dt> <dt>

[<span data-ttu-id="69cb5-127">**Interface IXpsOMImageBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-127">**IXpsOMImageBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)
</dt> <dt>

[<span data-ttu-id="69cb5-128">**Interface IXpsOMLinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-128">**IXpsOMLinearGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
</dt> <dt>

[<span data-ttu-id="69cb5-129">**Interface IXpsOMRadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-129">**IXpsOMRadialGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)
</dt> <dt>

[<span data-ttu-id="69cb5-130">**Interface IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-130">**IXpsOMSolidColorBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="69cb5-131">**Interface IXpsOMTileBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-131">**IXpsOMTileBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
</dt> <dt>

[<span data-ttu-id="69cb5-132">**Interface IXpsOMVisualBrush**</span><span class="sxs-lookup"><span data-stu-id="69cb5-132">**IXpsOMVisualBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
</dt> <dt>

[<span data-ttu-id="69cb5-133">**\_couleur XPS**</span><span class="sxs-lookup"><span data-stu-id="69cb5-133">**XPS\_COLOR**</span></span>](xps-color.md)
</dt> <dt>

[<span data-ttu-id="69cb5-134">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="69cb5-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



