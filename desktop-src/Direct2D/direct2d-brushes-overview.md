---
title: Présentation des pinceaux
description: Décrit les différents types de pinceaux fournis par Direct2D.
ms.assetid: 7a31d9e7-0521-40ee-b2c1-592dfaf5301e
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 7c8b4c4762a03650f150a74d3207d12767e1fb4e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383207"
---
# <a name="brushes-overview"></a><span data-ttu-id="fc299-103">Présentation des pinceaux</span><span class="sxs-lookup"><span data-stu-id="fc299-103">Brushes overview</span></span>

<span data-ttu-id="fc299-104">Cette vue d’ensemble décrit comment créer et utiliser des objets [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)et [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pour peindre des zones avec des couleurs unies, des dégradés et des bitmaps.</span><span class="sxs-lookup"><span data-stu-id="fc299-104">This overview describes how to create and use [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) objects to paint areas with solid colors, gradients, and bitmaps.</span></span> <span data-ttu-id="fc299-105">Elle contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="fc299-105">It contains the following sections.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fc299-106">Prérequis</span><span class="sxs-lookup"><span data-stu-id="fc299-106">Prerequisites</span></span>

<span data-ttu-id="fc299-107">Cette vue d’ensemble suppose que vous êtes familiarisé avec la structure d’une application Direct2D de base, comme décrit dans [création d’une application Direct2d simple](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="fc299-107">This overview assumes that you are familiar with the structure of a basic Direct2D application, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="brush-types"></a><span data-ttu-id="fc299-108">Types de pinceau</span><span class="sxs-lookup"><span data-stu-id="fc299-108">Brush types</span></span>

<span data-ttu-id="fc299-109">Un pinceau « peint » une zone avec sa sortie.</span><span class="sxs-lookup"><span data-stu-id="fc299-109">A brush "paints" an area with its output.</span></span> <span data-ttu-id="fc299-110">Des pinceaux différents ont différents types de sortie.</span><span class="sxs-lookup"><span data-stu-id="fc299-110">Different brushes have different types of output.</span></span> <span data-ttu-id="fc299-111">Direct2D fournit quatre types de pinceau : [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) peint une zone avec une couleur unie, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) avec un dégradé linéaire, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) avec un dégradé radial et [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) avec une bitmap.</span><span class="sxs-lookup"><span data-stu-id="fc299-111">Direct2D provides four brush types: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints an area with a solid color, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) with a linear gradient, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) with a radial gradient, and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with a bitmap.</span></span>

> [!NOTE]  
> <span data-ttu-id="fc299-112">À compter de Windows 8, vous pouvez également utiliser [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), qui est similaire à un pinceau bitmap, mais vous pouvez également utiliser des primitives.</span><span class="sxs-lookup"><span data-stu-id="fc299-112">Starting with Windows 8, you can also use [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), which is similar to a bitmap brush, but you can use primitives, too.</span></span>

<span data-ttu-id="fc299-113">Tous les pinceaux héritent de [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) et partagent un ensemble de fonctionnalités communes (définition et obtention d’opacité, et transformation de pinceaux). ils sont créés par [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) et sont des ressources dépendantes de l’appareil : votre application doit créer des pinceaux après avoir initialisé la cible de rendu avec laquelle les pinceaux seront utilisés, puis recréer les pinceaux chaque fois que la cible de rendu doit être recréée.</span><span class="sxs-lookup"><span data-stu-id="fc299-113">All brushes inherit from [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) and share a set of common features (setting and getting opacity, and transforming brushes); they are created by [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) and are device-dependent resources: your application should create brushes after it initializes the render target with which the brushes will be used, and recreate the brushes whenever the render target needs recreated.</span></span> <span data-ttu-id="fc299-114">(Pour plus d’informations sur les ressources, consultez [vue d’ensemble des ressources](resources-and-resource-domains.md).)</span><span class="sxs-lookup"><span data-stu-id="fc299-114">(For more information about resources, see [Resources Overview](resources-and-resource-domains.md).)</span></span>

<span data-ttu-id="fc299-115">L’illustration suivante montre des exemples de chacun des différents types de pinceau.</span><span class="sxs-lookup"><span data-stu-id="fc299-115">The following illustration shows examples of each of the different brush types.</span></span>

![illustration des effets visuels à partir des pinceaux de couleur unie, des pinceaux de dégradé linéaires, des pinceaux de dégradé radiaux et des pinceaux bitmap](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a><span data-ttu-id="fc299-117">Notions de base des couleurs</span><span class="sxs-lookup"><span data-stu-id="fc299-117">Color basics</span></span>

<span data-ttu-id="fc299-118">Avant de peindre avec un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ou un pinceau de dégradé, vous devez choisir des couleurs.</span><span class="sxs-lookup"><span data-stu-id="fc299-118">Before you paint with an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or a gradient brush, you need to choose colors.</span></span> <span data-ttu-id="fc299-119">Dans Direct2D, les couleurs sont représentées par la structure de [**\_ couleur d2d1 \_ F**](d2d1-color-f.md) (qui est en fait un nouveau nom pour la structure utilisée par Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).</span><span class="sxs-lookup"><span data-stu-id="fc299-119">In Direct2D, colors are represented by the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure (which is actually just a new name for the structure that is used by Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).</span></span>

<span data-ttu-id="fc299-120">Avant Windows 8, [**d2d1 \_ Color \_ F**](d2d1-color-f.md) utilise l’encodage sRVB.</span><span class="sxs-lookup"><span data-stu-id="fc299-120">Prior to Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) uses sRGB encoding.</span></span> <span data-ttu-id="fc299-121">l’encodage sRVB divise les couleurs en quatre composants : rouge, vert, bleu et alpha.</span><span class="sxs-lookup"><span data-stu-id="fc299-121">sRGB encoding divides colors into four components: red, green, blue, and alpha.</span></span> <span data-ttu-id="fc299-122">Chaque composant est représenté par une valeur de virgule flottante comprise dans une plage standard de 0 à 1.</span><span class="sxs-lookup"><span data-stu-id="fc299-122">Each component is represented by a floating point value with a normal range of 0.0 to 1.0.</span></span> <span data-ttu-id="fc299-123">La valeur 0 indique l’absence complète de cette couleur, tandis que la valeur 1 indique que cette couleur est entièrement présente.</span><span class="sxs-lookup"><span data-stu-id="fc299-123">A value of 0.0 indicates the complete absence of that color, while a value of 1.0 indicates that the color is fully present.</span></span> <span data-ttu-id="fc299-124">Pour le composant alpha, 0 représente une couleur totalement transparente, et 1 une couleur totalement opaque.</span><span class="sxs-lookup"><span data-stu-id="fc299-124">For the alpha component, 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span>

<span data-ttu-id="fc299-125">À partir de Windows 8, [**d2d1 \_ Color \_ F**](d2d1-color-f.md) accepte également l’encodage ScRVB.</span><span class="sxs-lookup"><span data-stu-id="fc299-125">Starting in Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) also accepts scRGB encoding.</span></span> <span data-ttu-id="fc299-126">ScRVB est un sur-ensemble de qui autorise les valeurs de couleur supérieures à 1,0 et inférieures à 0,0.</span><span class="sxs-lookup"><span data-stu-id="fc299-126">scRGB is a superset of that allows color values above 1.0 and below 0.0.</span></span>

<span data-ttu-id="fc299-127">Pour définir une couleur, vous pouvez utiliser la structure de [**\_ couleur d2d1 \_ F**](d2d1-color-f.md) et initialiser les champs vous-même, ou vous pouvez utiliser la classe [**d2d1 :: ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) pour vous aider à créer la couleur.</span><span class="sxs-lookup"><span data-stu-id="fc299-127">To define a color, you can use the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure and initialize its fields yourself, or you can use the [**D2D1::ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to help you create the color.</span></span> <span data-ttu-id="fc299-128">La classe **ColorF** fournit plusieurs constructeurs pour définir des couleurs.</span><span class="sxs-lookup"><span data-stu-id="fc299-128">The **ColorF** class provides several constructors for defining colors.</span></span> <span data-ttu-id="fc299-129">Si la valeur alpha n’est pas spécifiée dans les constructeurs, la valeur par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc299-129">If the alpha value is not specified in the constructors, it defaults to 1.0.</span></span>

-   <span data-ttu-id="fc299-130">Utilisez le constructeur [**ColorF (enum, float)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) pour spécifier une couleur prédéfinie et une valeur de canal alpha.</span><span class="sxs-lookup"><span data-stu-id="fc299-130">Use the [**ColorF(Enum, FLOAT)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) constructor to specify a predefined color and an alpha channel value.</span></span> <span data-ttu-id="fc299-131">Une valeur de canal alpha est comprise entre 0,0 et 1,0, où 0,0 représente une couleur entièrement transparente et 1,0 représente une couleur entièrement opaque.</span><span class="sxs-lookup"><span data-stu-id="fc299-131">An alpha channel value ranges from 0.0 to 1.0, where 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span> <span data-ttu-id="fc299-132">L’illustration suivante montre plusieurs couleurs prédéfinies et leurs équivalents hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="fc299-132">The following illustration shows several predefined colors and their hexadecimal equivalents.</span></span> <span data-ttu-id="fc299-133">Pour obtenir la liste complète des couleurs prédéfinies, consultez la section constantes de couleur de la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="fc299-133">For a complete list of predefined colors, see the Color constants section of the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span>

    ![illustration des couleurs prédéfinies](images/brushes-ovw-colors.png)

    <span data-ttu-id="fc299-135">L’exemple suivant crée une couleur prédéfinie et l’utilise pour spécifier la couleur d’un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="fc299-135">The following example creates a predefined color and uses it to specify the color of an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   <span data-ttu-id="fc299-136">Utilisez le constructeur [**ColorF (float, float, float, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) pour spécifier une couleur dans l’ordre des rouge, vert, bleu et alpha, où chaque élément a une valeur comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc299-136">Use the [**ColorF(FLOAT, FLOAT, FLOAT, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) constructor to specify a color in the sequence of a red, green, blue, and alpha, where each element has a value between 0.0 and 1.0.</span></span>

    <span data-ttu-id="fc299-137">L’exemple suivant spécifie les valeurs rouge, vert, bleu et alpha pour une couleur.</span><span class="sxs-lookup"><span data-stu-id="fc299-137">The following example specifies the red, green, blue, and alpha values for a color.</span></span>

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   <span data-ttu-id="fc299-138">Utilisez le constructeur [**ColorF (UInt32, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) pour spécifier la valeur hexadécimale d’une couleur et une valeur alpha, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="fc299-138">Use the [**ColorF(UINT32, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) constructor to specify the hexadecimal value of a color and an alpha value, as shown in the following example.</span></span>
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a><span data-ttu-id="fc299-139">Modes alpha</span><span class="sxs-lookup"><span data-stu-id="fc299-139">Alpha modes</span></span>

<span data-ttu-id="fc299-140">Quel que soit le mode Alpha de la cible de rendu avec lequel vous utilisez un pinceau, les valeurs de [**\_ couleur d2d1 \_ F**](d2d1-color-f.md) sont toujours interprétées comme des valeurs alpha directes.</span><span class="sxs-lookup"><span data-stu-id="fc299-140">Regardless of the alpha mode of the render target with which you use a brush, [**D2D1\_COLOR\_F**](d2d1-color-f.md) values are always interpreted as straight alpha.</span></span>

## <a name="using-solid-color-brushes"></a><span data-ttu-id="fc299-141">Utilisation de pinceaux de couleur unie</span><span class="sxs-lookup"><span data-stu-id="fc299-141">Using solid color brushes</span></span>

<span data-ttu-id="fc299-142">Pour créer un pinceau de couleur unie, appelez la méthode [**ID2D1RenderTarget :: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , qui retourne un HRESULT et un objet [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) .</span><span class="sxs-lookup"><span data-stu-id="fc299-142">To create a solid color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method, which returns an HRESULT and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) object.</span></span> <span data-ttu-id="fc299-143">L’illustration suivante montre un carré qui est rayé avec un pinceau de couleur noir et peint avec un pinceau de couleur unie qui a la valeur de couleur de 0x9ACD32.</span><span class="sxs-lookup"><span data-stu-id="fc299-143">The following illustration shows a square that is stroked with a black color brush and painted with a solid color brush that has the color value of 0x9ACD32.</span></span>

![illustration d’un carré peint avec un pinceau de couleur unie](images/brushes-ovw-solidcolor.png)

<span data-ttu-id="fc299-145">Le code suivant montre comment créer et utiliser un pinceau de couleur noire et un pinceau avec une valeur de couleur de 0x9ACD32 pour remplir et dessiner ce carré.</span><span class="sxs-lookup"><span data-stu-id="fc299-145">The following code shows how to create and use a black color brush and a brush with a color value of 0x9ACD32 to fill and draw this square.</span></span>


```C++
    ID2D1SolidColorBrush *m_pBlackBrush;
    ID2D1SolidColorBrush *m_pYellowGreenBrush;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
        &m_pBlackBrush
        );
}

// Create a solid color brush with its rgb value 0x9ACD32.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
}
```




```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
```



<span data-ttu-id="fc299-146">Contrairement à d’autres pinceaux, la création d’un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) est une opération relativement peu coûteuse.</span><span class="sxs-lookup"><span data-stu-id="fc299-146">Unlike other brushes, creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is a relatively inexpensive operation.</span></span> <span data-ttu-id="fc299-147">Vous pouvez créer des objets **ID2D1SolidColorBrush** chaque fois que vous affichez avec un faible impact sur les performances.</span><span class="sxs-lookup"><span data-stu-id="fc299-147">You may create **ID2D1SolidColorBrush** objects each time you render with little to no performance impact.</span></span> <span data-ttu-id="fc299-148">Cette approche n’est pas recommandée pour les pinceaux de dégradé ou de bitmap.</span><span class="sxs-lookup"><span data-stu-id="fc299-148">This approach is not recommended for gradient or bitmap brushes.</span></span>

## <a name="using-linear-gradient-brushes"></a><span data-ttu-id="fc299-149">Utilisation de pinceaux de dégradé linéaire</span><span class="sxs-lookup"><span data-stu-id="fc299-149">Using linear gradient brushes</span></span>

<span data-ttu-id="fc299-150">Un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) peint une zone avec un dégradé linéaire défini le long d’une ligne, l’axe du dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-150">An [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) paints an area with a linear gradient defined along a line, the gradient axis.</span></span> <span data-ttu-id="fc299-151">Vous spécifiez les couleurs du dégradé et leur emplacement le long de l’axe du dégradé à l’aide des objets [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) .</span><span class="sxs-lookup"><span data-stu-id="fc299-151">You specify the gradient's colors and their location along the gradient axis using [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) objects.</span></span> <span data-ttu-id="fc299-152">Vous pouvez également modifier l’axe du dégradé, ce qui vous permet de créer des dégradés horizontaux et verticaux et d’inverser le sens du dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-152">You may also modify the gradient axis, which enables you to create horizontal and vertical gradient and to reverse the gradient direction.</span></span> <span data-ttu-id="fc299-153">Pour créer un pinceau de dégradé linéaire, appelez la méthode [**ID2D1RenderTarget :: CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) .</span><span class="sxs-lookup"><span data-stu-id="fc299-153">To create a linear gradient brush, call the [**ID2D1RenderTarget::CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method.</span></span>

<span data-ttu-id="fc299-154">L’illustration suivante montre un carré qui est peint avec un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) avec deux couleurs prédéfinies, « jaune » et « ForestGreen ».</span><span class="sxs-lookup"><span data-stu-id="fc299-154">The following illustration shows a square that is painted with an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that has two predefined colors, "Yellow" and "ForestGreen".</span></span>

![illustration d’un carré peint avec un pinceau de dégradé linéaire jaune et de forêt vert](images/brushes-ovw-lineargradient.png)

<span data-ttu-id="fc299-156">Pour créer le dégradé présenté dans l’illustration précédente, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="fc299-156">To create the gradient shown in the preceding illustration, complete these steps:</span></span>

1.  <span data-ttu-id="fc299-157">Déclarez deux objets [**d2d1 \_ \_ Stop gradient**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="fc299-157">Declare two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="fc299-158">Chaque point de dégradé spécifie une couleur et une position.</span><span class="sxs-lookup"><span data-stu-id="fc299-158">Each gradient stop specifies a color and a position.</span></span> <span data-ttu-id="fc299-159">Une position de 0,0 indique le début du dégradé, tandis qu’une position de 1,0 indique la fin du dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-159">A position of 0.0 indicates the beginning of the gradient, while a position of 1.0 indicates the end of the gradient.</span></span>

    <span data-ttu-id="fc299-160">Le code suivant crée un tableau de deux [**objets \_ d2d1 \_ Stop gradient**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="fc299-160">The following code creates an array of two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="fc299-161">La première étape spécifie la couleur « jaune » à la position 0, tandis que la deuxième Stop spécifie la couleur « ForestGreen » à la position 1.</span><span class="sxs-lookup"><span data-stu-id="fc299-161">The first stop specifies the color "Yellow" at a position 0, and the second stop specifies the color "ForestGreen" at position 1.</span></span>

```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
```

    

2.  <span data-ttu-id="fc299-162">Créez un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span><span class="sxs-lookup"><span data-stu-id="fc299-162">Create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span> <span data-ttu-id="fc299-163">L’exemple suivant appelle [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), en passant le tableau d’objets [**d2d1 \_ gradient \_ Stop**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) , le nombre de points de dégradé (2), le [**\_ gamma d2d1 \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) pour l’interpolation et le [**\_ \_ mode \_ d’extension d2d1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) pour le mode Extend.</span><span class="sxs-lookup"><span data-stu-id="fc299-163">The following example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), passing in the array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects, the number of gradient stops (2), [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) for interpolation, and [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) for the extend mode.</span></span>

```C++
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

    

3.  <span data-ttu-id="fc299-164">Créez le [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="fc299-164">Create the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="fc299-165">L’exemple suivant appelle la méthode [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) et lui transmet les propriétés de pinceau de dégradé linéaire qui contiennent le point de départ à (0, 0) et le point de terminaison à (150, 150), et les points de dégradé créés à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="fc299-165">The next example calls the [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method and passes it the linear gradient brush properties that contain the start point at (0, 0) and the end point at (150, 150), and the gradient stops created in the previous step.</span></span>
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

    

4.  <span data-ttu-id="fc299-166">Utilisez [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="fc299-166">Use the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="fc299-167">L’exemple de code suivant utilise le pinceau pour remplissage du un rectangle.</span><span class="sxs-lookup"><span data-stu-id="fc299-167">The next code example uses the brush to fille a rectangle.</span></span>
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a><span data-ttu-id="fc299-168">En savoir plus sur les arrêts de dégradé</span><span class="sxs-lookup"><span data-stu-id="fc299-168">More about gradient stops</span></span>

<span data-ttu-id="fc299-169">Le [**\_ \_ point de dégradé d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) est le bloc de construction de base d’un pinceau de dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-169">The [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) is the basic building block of a gradient brush.</span></span> <span data-ttu-id="fc299-170">Un point de dégradé spécifie la couleur et la position le long de l’axe du dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-170">A gradient stop specifies the color and the position along the gradient axis.</span></span> <span data-ttu-id="fc299-171">La valeur de la position du dégradé est comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc299-171">The value of the gradient position ranges between 0.0 and 1.0.</span></span> <span data-ttu-id="fc299-172">Plus il est proche de 0,0, plus la couleur est proche du début du dégradé. plus la valeur est proche de 1,0, plus la couleur est proche de la fin du dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-172">The closer it is to 0.0, the closer the color is to the start of the gradient; the closer it is to 1.0, the closer the color is to the end of the gradient.</span></span>

<span data-ttu-id="fc299-173">L’illustration suivante met en évidence les points de dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-173">The following illustration highlights the gradient stops.</span></span> <span data-ttu-id="fc299-174">Le cercle marque la position des points de dégradé et une ligne en pointillés affiche l’axe du dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-174">The circle marks the position of gradient stops and a dashed line shows the gradient axis.</span></span>

![illustration d’un pinceau de dégradé linéaire avec quatre arrêts le long de l’axe](images/4stoplineargradient.png)

<span data-ttu-id="fc299-176">Le premier point de dégradé spécifie la couleur jaune à une position de 0,0.</span><span class="sxs-lookup"><span data-stu-id="fc299-176">The first gradient stop specifies the color yellow at a position of 0.0.</span></span> <span data-ttu-id="fc299-177">Le deuxième point de dégradé spécifie la couleur rouge à une position de 0,25.</span><span class="sxs-lookup"><span data-stu-id="fc299-177">The second gradient stop specifies red color at a position of 0.25.</span></span> <span data-ttu-id="fc299-178">De la gauche vers la droite le long de l’axe du dégradé, les couleurs entre ces deux arrêts passent progressivement du jaune au rouge.</span><span class="sxs-lookup"><span data-stu-id="fc299-178">From left to right along the gradient axis, the colors between these two stops gradually change from yellow to red.</span></span> <span data-ttu-id="fc299-179">Le troisième point de dégradé spécifie la couleur bleue à une position de 0,75.</span><span class="sxs-lookup"><span data-stu-id="fc299-179">The third gradient stop specifies blue color at a position of 0.75.</span></span> <span data-ttu-id="fc299-180">Les couleurs entre les deuxième et troisième points de dégradé passent progressivement du rouge au bleu.</span><span class="sxs-lookup"><span data-stu-id="fc299-180">The colors between the second and third gradient stops gradually change from red to blue.</span></span> <span data-ttu-id="fc299-181">Le quatrième point de dégradé spécifie vert citron vert à une position de 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc299-181">The fourth gradient stop specifies lime green at a position of 1.0.</span></span> <span data-ttu-id="fc299-182">Les couleurs entre les troisième et quatrième points de dégradé passent progressivement du bleu au vert citron.</span><span class="sxs-lookup"><span data-stu-id="fc299-182">The colors between the third and fourth gradient stops gradually change from blue to lime green.</span></span>

## <a name="the-gradient-axis"></a><span data-ttu-id="fc299-183">Axe du dégradé</span><span class="sxs-lookup"><span data-stu-id="fc299-183">The gradient axis</span></span>

<span data-ttu-id="fc299-184">Comme mentionné précédemment, les points de dégradé d’un pinceau de dégradé linéaire sont positionnés le long d’une ligne, l’axe du dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-184">As mentioned previously, gradient stops of a linear gradient brush are positioned along a line, the gradient axis.</span></span> <span data-ttu-id="fc299-185">Vous pouvez spécifier l’orientation et la taille de la ligne à l’aide des champs **StartPoint** et **Endpoint** de la structure de [**Propriétés de \_ \_ \_ pinceau \_ de dégradé linéaire d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) lorsque vous créez un pinceau de dégradé linéaire.</span><span class="sxs-lookup"><span data-stu-id="fc299-185">You can specify the orientation and size of the line using the **startPoint** and **endPoint** fields of the [**D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) structure when you create a linear gradient brush.</span></span> <span data-ttu-id="fc299-186">Une fois que vous avez créé un pinceau, vous pouvez ajuster l’axe du dégradé en appelant les méthodes [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) et [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) du pinceau.</span><span class="sxs-lookup"><span data-stu-id="fc299-186">After you've created a brush, you can adjust the gradient axis by calling the brush's [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) and [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) methods.</span></span> <span data-ttu-id="fc299-187">En manipulant le point de départ et le point de terminaison du pinceau, vous pouvez créer des dégradés horizontaux et verticaux, inverser le sens du dégradé et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="fc299-187">By manipulating the brush's start point and end point, you can create horizontal and vertical gradients, reverse the gradient direction, and more.</span></span>

<span data-ttu-id="fc299-188">Par exemple, dans l’illustration suivante, le point de départ est défini sur (0, 0) et le point de terminaison sur (150, 50); Cela crée un dégradé Diagonal qui commence à l’angle supérieur gauche et s’étend jusqu’au coin inférieur droit de la zone qui est peinte.</span><span class="sxs-lookup"><span data-stu-id="fc299-188">For example, in the following illustration, the start point is set to (0,0) and the end point to (150, 50); this creates a diagonal gradient that starts at the upper-left corner and extends to the lower-right corner of the area being painted.</span></span> <span data-ttu-id="fc299-189">Lorsque vous définissez le point de départ sur (0, 25) et le point de terminaison sur (150, 25), un dégradé horizontal est créé.</span><span class="sxs-lookup"><span data-stu-id="fc299-189">When you set the start point to (0, 25) and the end point to (150, 25), a horizontal gradient is created.</span></span> <span data-ttu-id="fc299-190">De même, la définition du point de départ sur (75, 0) et le point de terminaison sur (75, 50) crée un dégradé vertical.</span><span class="sxs-lookup"><span data-stu-id="fc299-190">Similarly, setting the start point to (75, 0) and the end point to (75, 50) creates a vertical gradient.</span></span> <span data-ttu-id="fc299-191">Le fait de définir le point de départ sur (0, 50) et le point de terminaison sur (150, 0) crée un dégradé Diagonal qui commence dans le coin inférieur gauche et s’étend jusqu’au coin supérieur droit de la zone qui est peinte.</span><span class="sxs-lookup"><span data-stu-id="fc299-191">Setting the start point to (0, 50) and the end point to (150, 0) creates a diagonal gradient that starts at the lower-left corner and extends to the upper-right corner of the area being painted.</span></span>

![illustration de quatre axes de dégradé différents dans le même rectangle](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a><span data-ttu-id="fc299-193">Utilisation de pinceaux de dégradé radiaux</span><span class="sxs-lookup"><span data-stu-id="fc299-193">Using radial gradient brushes</span></span>

<span data-ttu-id="fc299-194">Contrairement à un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), qui fusionne deux couleurs ou plus sur un axe de dégradé, un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) peint une zone avec un dégradé radial qui fusionne deux couleurs ou plus sur une ellipse.</span><span class="sxs-lookup"><span data-stu-id="fc299-194">Unlike an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), which blends two or more colors along a gradient axis, an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) paints an area with a radial gradient that blends two or more colors across an ellipse.</span></span> <span data-ttu-id="fc299-195">Tandis qu’un **ID2D1LinearGradientBrush** définit son axe de dégradé avec un point de départ et un point de terminaison, un **ID2D1RadialGradientBrush** définit son ellipse de dégradé en spécifiant un rayon centré, horizontal et vertical, ainsi qu’un décalage de l’origine du dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-195">While a **ID2D1LinearGradientBrush** defines its gradient axis with a start point and an end point, a **ID2D1RadialGradientBrush** defines its gradient ellipse by specifying a center, horizontal and vertical radii, and a gradient origin offset.</span></span>

<span data-ttu-id="fc299-196">À l’instar d’un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) utilise un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) pour spécifier les couleurs et les positions dans le dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-196">Like an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) uses an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to specify the colors and positions in the gradient.</span></span>

<span data-ttu-id="fc299-197">L’illustration suivante montre un cercle peint avec un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="fc299-197">The following illustration shows a circle painted with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span> <span data-ttu-id="fc299-198">Le cercle comporte deux points de dégradé : le premier spécifie une couleur prédéfinie « jaune » à la position 0,0 et le second spécifie une couleur prédéfinie « ForestGreen » à une position de 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc299-198">The circle has two gradient stops: the first specifies a predefined color "Yellow" at a position of 0.0, and the second specifies a predefined color "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="fc299-199">Le dégradé a un centre de (75, 75), un décalage d’origine du dégradé (0, 0) et un rayon x et y de 75.</span><span class="sxs-lookup"><span data-stu-id="fc299-199">The gradient has a center of (75, 75), a gradient origin offset of (0, 0), and an x- and y-radius of 75.</span></span>

![illustration d’un cercle peint avec un pinceau dégradé radial](images/brushes-ovw-radials.png)

<span data-ttu-id="fc299-201">Les exemples de code suivants montrent comment peindre ce cercle avec un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) qui a deux arrêts de couleur : « jaune » à une position de 0,0 et « ForestGreen » à une position de 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc299-201">The following code examples shows how to paint this circle with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that has two color stops: "Yellow" at a position of 0.0, and "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="fc299-202">Comme pour la création d’un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), l’exemple appelle [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) pour créer un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) à partir d’un tableau de points de dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-202">Similar to creating an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), the example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from an array of gradient stops.</span></span>


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



<span data-ttu-id="fc299-203">Pour créer un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), utilisez la méthode [**ID2D1RenderTarget :: CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="fc299-203">To create an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), use the [**ID2D1RenderTarget::CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) method.</span></span> <span data-ttu-id="fc299-204">**CreateRadialGradientBrush** prend trois paramètres.</span><span class="sxs-lookup"><span data-stu-id="fc299-204">The **CreateRadialGradientBrush** takes three parameters.</span></span> <span data-ttu-id="fc299-205">Le premier paramètre, les [**\_ Propriétés de \_ \_ pinceau \_ de dégradé radial d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) spécifie le centre, le décalage d’origine du dégradé et les rayons horizontaux et verticaux du dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-205">The first parameter, a [**D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) specifies the center, gradient origin offset, and the horizontal and vertical radii of the gradient.</span></span> <span data-ttu-id="fc299-206">Le deuxième paramètre est un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) qui décrit les couleurs et leurs positions dans le dégradé, tandis que le troisième paramètre est l’adresse du pointeur qui reçoit la nouvelle référence **ID2D1RadialGradientBrush** .</span><span class="sxs-lookup"><span data-stu-id="fc299-206">The second parameter is an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) that describes the colors and their positions in the gradient, and the third parameter is the address of the pointer that receive the new **ID2D1RadialGradientBrush** reference.</span></span> <span data-ttu-id="fc299-207">Certaines surcharges prennent un paramètre supplémentaire, une structure de [**\_ \_ Propriétés de pinceau d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) qui spécifie une valeur d’opacité et une transformation à appliquer au nouveau pinceau.</span><span class="sxs-lookup"><span data-stu-id="fc299-207">Some overloads take an additional parameter, a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) structure that specifies an opacity value and a transform to apply to the new brush.</span></span>

<span data-ttu-id="fc299-208">L’exemple suivant appelle [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), en passant le tableau de points de dégradé et les propriétés de pinceau de dégradé radial dont la valeur *Center* est définie sur (75, 75), le *gradientOriginOffset* défini sur (0, 0) *et* *RadiusX et RadiusY* ont tous les deux la valeur 75.</span><span class="sxs-lookup"><span data-stu-id="fc299-208">The next example calls [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), passing in the array of gradient stops, and the radial gradient brush properties that have the *center* value set to (75, 75), the *gradientOriginOffset* set to (0, 0), and *radiusX* and *radiusY* both set to 75.</span></span>


```C++
// The center of the gradient is in the center of the box.
// The gradient origin offset was set to zero(0, 0) or center in this case.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateRadialGradientBrush(
        D2D1::RadialGradientBrushProperties(
            D2D1::Point2F(75, 75),
            D2D1::Point2F(0, 0),
            75,
            75),
        pGradientStops,
        &m_pRadialGradientBrush
        );
}
```



<span data-ttu-id="fc299-209">L’exemple final utilise le pinceau pour remplir une ellipse.</span><span class="sxs-lookup"><span data-stu-id="fc299-209">The final example uses the brush to fill an ellipse.</span></span>


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a><span data-ttu-id="fc299-210">Configuration d’un dégradé radial</span><span class="sxs-lookup"><span data-stu-id="fc299-210">Configuring a radial gradient</span></span>

<span data-ttu-id="fc299-211">Les valeurs différentes pour *Center*, *gradientOriginOffset*, *RadiusX* et/ou *RadiusY* produisent différents dégradés.</span><span class="sxs-lookup"><span data-stu-id="fc299-211">Different values for *center*, *gradientOriginOffset*, *radiusX* and/or *radiusY* produce different gradients.</span></span> <span data-ttu-id="fc299-212">L’illustration suivante montre plusieurs dégradés radiaux qui ont des décalages d’origine du dégradé différents, créant ainsi l’apparence de la lumière éclairant les cercles à partir de différents angles.</span><span class="sxs-lookup"><span data-stu-id="fc299-212">The following illustration shows several radial gradients that have different gradient origin offsets, creating the appearance of the light illuminating the circles from different angles.</span></span>

![illustration du même cercle peint avec des pinceaux de dégradé radiaux avec des décalages d’origine différents](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a><span data-ttu-id="fc299-214">Utilisation de pinceaux bitmap</span><span class="sxs-lookup"><span data-stu-id="fc299-214">Using bitmap brushes</span></span>

<span data-ttu-id="fc299-215">Un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) peint une zone avec une image bitmap (représentée par un objet [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ).</span><span class="sxs-lookup"><span data-stu-id="fc299-215">An [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) paints an area with a bitmap (represented by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object).</span></span>

<span data-ttu-id="fc299-216">L’illustration suivante montre un carré peint avec une image bitmap d’une usine.</span><span class="sxs-lookup"><span data-stu-id="fc299-216">The following illustration shows a square painted with a bitmap of a plant.</span></span>

![illustration d’un carré peint avec une image bitmap de plante](images/brushes-ovw-bitmap.png)

<span data-ttu-id="fc299-218">Les exemples qui suivent montrent comment peindre ce carré avec un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="fc299-218">The examples that follow shows how to paint this square with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>

<span data-ttu-id="fc299-219">Le premier exemple Initialise un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) à utiliser avec le pinceau.</span><span class="sxs-lookup"><span data-stu-id="fc299-219">The first example initializes an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) for use with the brush.</span></span> <span data-ttu-id="fc299-220">Le **ID2D1Bitmap** est fourni par une méthode d’assistance, LoadResourceBitmap, définie ailleurs dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="fc299-220">The **ID2D1Bitmap** is provided by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
}
```



<span data-ttu-id="fc299-221">Pour créer le pinceau bitmap, appelez la méthode [**ID2D1RenderTarget :: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) et spécifiez le [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) à peindre.</span><span class="sxs-lookup"><span data-stu-id="fc299-221">To create the bitmap brush, call the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with which to paint.</span></span> <span data-ttu-id="fc299-222">La méthode retourne un **HRESULT** et un objet [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) .</span><span class="sxs-lookup"><span data-stu-id="fc299-222">The method returns an **HRESULT** and an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) object.</span></span> <span data-ttu-id="fc299-223">Certaines surcharges de **CreateBitmapBrush** vous permettent de spécifier des options supplémentaires en acceptant des [**\_ \_ Propriétés de pinceau d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) et une structure de [**Propriétés de \_ \_ pinceau \_ de bitmap d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) .</span><span class="sxs-lookup"><span data-stu-id="fc299-223">Some **CreateBitmapBrush** overloads enable you to specify additional options by accepting a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) and a [**D2D1\_BITMAP\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) structure.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



<span data-ttu-id="fc299-224">L’exemple suivant utilise le pinceau pour remplir un rectangle.</span><span class="sxs-lookup"><span data-stu-id="fc299-224">The next example uses the brush to fill a rectangle.</span></span>


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a><span data-ttu-id="fc299-225">Configuration des modes d’extension</span><span class="sxs-lookup"><span data-stu-id="fc299-225">Configuring extend modes</span></span>

<span data-ttu-id="fc299-226">Parfois, le dégradé d’un pinceau de dégradé ou de l’image bitmap pour un pinceau bitmap ne remplit pas complètement la zone qui est peinte.</span><span class="sxs-lookup"><span data-stu-id="fc299-226">Sometimes, the gradient of a gradient brush or the bitmap for a bitmap brush doesn't completely fill the area being painted.</span></span>

-   <span data-ttu-id="fc299-227">Lorsque cela se produit pour un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D utilise les paramètres du mode d’extension horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) et vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) du pinceau pour déterminer comment remplir la zone restante.</span><span class="sxs-lookup"><span data-stu-id="fc299-227">When this happens for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D uses the brush's horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) and vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) extend mode settings to determine how to fill the remaining area.</span></span>

-   <span data-ttu-id="fc299-228">Lorsque cela se produit pour un pinceau de dégradé, Direct2D détermine comment remplir la zone restante à l’aide de la valeur du paramètre du [**\_ \_ mode d’extension d2d1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) que vous avez spécifié quand vous avez appelé le [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) pour créer le [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)du pinceau de dégradé.</span><span class="sxs-lookup"><span data-stu-id="fc299-228">When this happens for a gradient brush, Direct2D determines how to fill the remaining area by using the value of the [**D2D1\_EXTEND\_MODE**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) parameter that you specified when you called the [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create the gradient brush's [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>

<span data-ttu-id="fc299-229">L’illustration suivante montre les résultats de chaque combinaison possible des modes d’extension pour un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**d2d1 \_ \_ en mode \_ extension**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (clamp), **d2d1 \_ mode d’extension \_ \_ Wrap** (Wrap) et **d2d1 \_ étendre le \_ miroir** (miroir).</span><span class="sxs-lookup"><span data-stu-id="fc299-229">The following illustration shows the results from every possible combination of the extend modes for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (CLAMP), **D2D1\_EXTEND\_MODE\_WRAP** (WRAP), and **D2D1\_EXTEND\_MIRROR** (MIRROR).</span></span>

![illustration d’une image d’origine et des images obtenues à partir de différents modes d’extension](images/bitmapwrap-clamp-mirror.png)

<span data-ttu-id="fc299-231">L’exemple suivant montre comment définir les modes d’extension x et y du pinceau bitmap sur [**d2d1 étendre le \_ \_ miroir**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="fc299-231">The following example shows how to set the bitmap brush's x- and y-extend modes to [**D2D1\_EXTEND\_MIRROR**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span> <span data-ttu-id="fc299-232">Il peint ensuite le rectangle avec le [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="fc299-232">It then paints the rectangle with the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



<span data-ttu-id="fc299-233">Il produit une sortie comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="fc299-233">It produces output as shown in the following illustration.</span></span>

![illustration d’une image d’origine et de l’image résultante après la mise en miroir de l’axe x et de l’axe y](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a><span data-ttu-id="fc299-235">Transformer des pinceaux</span><span class="sxs-lookup"><span data-stu-id="fc299-235">Transforming brushes</span></span>

<span data-ttu-id="fc299-236">Quand vous peignez avec un pinceau, il peint l’espace de coordonnées de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="fc299-236">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="fc299-237">Les pinceaux ne se positionnent pas automatiquement pour s’aligner avec l’objet qui est peint ; par défaut, ils commencent à peindre à l’origine (0,0) de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="fc299-237">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="fc299-238">Vous pouvez « déplacer » le dégradé défini par un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) vers une zone cible en définissant son point de départ et son point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="fc299-238">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="fc299-239">De même, vous pouvez déplacer le dégradé défini par un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) en modifiant son centre et ses rayons.</span><span class="sxs-lookup"><span data-stu-id="fc299-239">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="fc299-240">Pour aligner le contenu d’un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) sur la zone qui est peinte, vous pouvez utiliser la méthode [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) pour convertir l’image bitmap à l’emplacement souhaité.</span><span class="sxs-lookup"><span data-stu-id="fc299-240">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="fc299-241">Cette transformation affecte uniquement le pinceau ; elle n’affecte pas les autres contenus dessinés par la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="fc299-241">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="fc299-242">Les illustrations suivantes montrent l’effet de l’utilisation d’un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pour remplir un rectangle situé à l’emplacement (100, 100).</span><span class="sxs-lookup"><span data-stu-id="fc299-242">The following illustrations shows the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="fc299-243">L’illustration de l’illustration de gauche montre le résultat du remplissage du rectangle sans transformer le pinceau : le bitmap est dessiné à l’origine de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="fc299-243">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="fc299-244">Par conséquent, seule une partie de la bitmap apparaît dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="fc299-244">As a result, only a portion of the bitmap appears in the rectangle.</span></span> <span data-ttu-id="fc299-245">L’illustration à droite montre le résultat de la transformation du **ID2D1BitmapBrush** afin que son contenu soit décalé de 50 pixels vers la droite et de 50 pixels vers le dessous.</span><span class="sxs-lookup"><span data-stu-id="fc299-245">The illustration on the right shows the result of transforming the **ID2D1BitmapBrush** so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="fc299-246">Le bitmap remplit maintenant le rectangle.</span><span class="sxs-lookup"><span data-stu-id="fc299-246">The bitmap now fills the rectangle.</span></span>

![illustration d’un carré peint avec un pinceau bitmap sans transformer le pinceau et en transformant le pinceau](images/brushes-ovw-transform.png)

<span data-ttu-id="fc299-248">Le code suivant montre comment effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="fc299-248">The following code shows how to accomplish this.</span></span> <span data-ttu-id="fc299-249">Tout d’abord, appliquez une translation à la [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), en déplaçant le pinceau 50 pixels vers la droite le long de l’axe x et 50 pixels vers le côté de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="fc299-249">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="fc299-250">Utilisez ensuite le **ID2D1BitmapBrush** pour remplir le rectangle qui a l’angle supérieur gauche à (100, 100) et le coin inférieur droit à (200, 200).</span><span class="sxs-lookup"><span data-stu-id="fc299-250">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


```cpp
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
   
}

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}

D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);

// Demonstrate the effect of transforming a bitmap brush.
m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

// To see the content of the rcTransformedBrushRect, comment
// out this statement.
m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

m_pRenderTarget->DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```

## <a name="related-topics"></a><span data-ttu-id="fc299-251">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc299-251">Related topics</span></span>

* [<span data-ttu-id="fc299-252">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="fc299-252">Direct2D reference</span></span>](reference.md)
* [<span data-ttu-id="fc299-253">Comment créer un pinceau de couleur unie</span><span class="sxs-lookup"><span data-stu-id="fc299-253">How to create a solid color brush</span></span>](how-to-create-a-solid-color-brush.md)
* [<span data-ttu-id="fc299-254">Comment créer un pinceau de dégradé linéaire</span><span class="sxs-lookup"><span data-stu-id="fc299-254">How to create a linear gradient brush</span></span>](how-to-create-a-linear-gradient-brush.md)
* [<span data-ttu-id="fc299-255">Comment créer un pinceau de dégradé radial</span><span class="sxs-lookup"><span data-stu-id="fc299-255">How to create a radial gradient brush</span></span>](how-to-create-a-radial-gradient-brush.md)
* [<span data-ttu-id="fc299-256">Comment créer un pinceau bitmap</span><span class="sxs-lookup"><span data-stu-id="fc299-256">How to create a bitmap brush</span></span>](how-to-create-a-bitmap-brush.md)
