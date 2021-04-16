---
title: Vue d'ensemble des masques d'opacité
description: Cette rubrique explique comment utiliser des bitmaps et des pinceaux pour définir des masques d’opacité. Elle contient les sections suivantes.
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a4757a30247da465e0ae5226bd923219e3e665
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104550062"
---
# <a name="opacity-masks-overview"></a><span data-ttu-id="3fb27-104">Vue d'ensemble des masques d'opacité</span><span class="sxs-lookup"><span data-stu-id="3fb27-104">Opacity Masks Overview</span></span>

<span data-ttu-id="3fb27-105">Cette rubrique explique comment utiliser des bitmaps et des pinceaux pour définir des masques d’opacité.</span><span class="sxs-lookup"><span data-stu-id="3fb27-105">This topic describes how to use bitmaps and brushes to define opacity masks.</span></span> <span data-ttu-id="3fb27-106">Elle contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3fb27-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="3fb27-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="3fb27-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="3fb27-108">Qu’est-ce qu’un masque d’opacité ?</span><span class="sxs-lookup"><span data-stu-id="3fb27-108">What Is an Opacity Mask?</span></span>](#what-is-an-opacity-mask)
-   [<span data-ttu-id="3fb27-109">Utiliser une image bitmap comme masque d’opacité avec la méthode FillOpacityMask</span><span class="sxs-lookup"><span data-stu-id="3fb27-109">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [<span data-ttu-id="3fb27-110">Utiliser un pinceau comme masque d’opacité avec la méthode FillGeometry</span><span class="sxs-lookup"><span data-stu-id="3fb27-110">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [<span data-ttu-id="3fb27-111">Utiliser un pinceau de dégradé linéaire comme masque d’opacité</span><span class="sxs-lookup"><span data-stu-id="3fb27-111">Use an Linear Gradient Brush as an Opacity Mask</span></span>](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [<span data-ttu-id="3fb27-112">Utiliser un pinceau de dégradé radial comme masque d’opacité</span><span class="sxs-lookup"><span data-stu-id="3fb27-112">Use a Radial Gradient Brush as an Opacity Mask</span></span>](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [<span data-ttu-id="3fb27-113">Appliquer un masque d’opacité à une couche</span><span class="sxs-lookup"><span data-stu-id="3fb27-113">Apply an Opacity Mask to a Layer</span></span>](#apply-an-opacity-mask-to-a-layer)
-   [<span data-ttu-id="3fb27-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3fb27-114">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="3fb27-115">Prérequis</span><span class="sxs-lookup"><span data-stu-id="3fb27-115">Prerequisites</span></span>

<span data-ttu-id="3fb27-116">Cette vue d’ensemble suppose que vous êtes familiarisé avec les opérations de dessin Direct2D de base, comme décrit dans la procédure pas à pas [création d’une application Direct2d simple](direct2d-quickstart.md) .</span><span class="sxs-lookup"><span data-stu-id="3fb27-116">This overview assumes that you are familiar with basic Direct2D drawing operations, as described in the [Creating a Simple Direct2D Application](direct2d-quickstart.md) walkthrough.</span></span> <span data-ttu-id="3fb27-117">Vous devez également être familiarisé avec les différents types de pinceaux, comme décrit dans la [vue d’ensemble des pinceaux](direct2d-brushes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3fb27-117">You should also be familiar with the different types of brushes, as described in the [Brushes Overview](direct2d-brushes-overview.md).</span></span>

## <a name="what-is-an-opacity-mask"></a><span data-ttu-id="3fb27-118">Qu’est-ce qu’un masque d’opacité ?</span><span class="sxs-lookup"><span data-stu-id="3fb27-118">What Is an Opacity Mask?</span></span>

<span data-ttu-id="3fb27-119">Un masque d’opacité est un masque, décrit par un pinceau ou un bitmap, qui est appliqué à un autre objet pour rendre cet objet partiellement ou complètement transparent.</span><span class="sxs-lookup"><span data-stu-id="3fb27-119">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="3fb27-120">Un masque d’opacité utilise des informations de canal alpha pour spécifier la façon dont les pixels source de l’objet sont fusionnés dans la cible de destination finale.</span><span class="sxs-lookup"><span data-stu-id="3fb27-120">An opacity mask uses alpha channel information to specify how the source pixels of the object are blended into the final destination target.</span></span> <span data-ttu-id="3fb27-121">Les parties transparentes du masque indiquent les zones où l’image sous-jacente est masquée, tandis que les parties opaques du masque indiquent où l’objet masqué est visible.</span><span class="sxs-lookup"><span data-stu-id="3fb27-121">The transparent portions of the mask indicate the areas where the underlying image is hidden, whereas the opaque portions of the mask indicate where the masked object is visible.</span></span>

<span data-ttu-id="3fb27-122">Il existe plusieurs façons d’appliquer un masque d’opacité :</span><span class="sxs-lookup"><span data-stu-id="3fb27-122">There are several ways to apply an opacity mask:</span></span>

-   <span data-ttu-id="3fb27-123">Utilisez la méthode [**ID2D1RenderTarget :: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .</span><span class="sxs-lookup"><span data-stu-id="3fb27-123">Use the [**ID2D1RenderTarget::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method.</span></span> <span data-ttu-id="3fb27-124">La méthode **FillOpacityMask** peint une zone rectangulaire d’une cible de rendu, puis applique un masque d’opacité, défini par une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="3fb27-124">The **FillOpacityMask** method paints a rectangular region of a render target and then applies an opacity mask, defined by a bitmap.</span></span> <span data-ttu-id="3fb27-125">Utilisez cette méthode lorsque votre masque d’opacité est un bitmap et que vous souhaitez remplir une zone rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="3fb27-125">Use this method when your opacity mask is a bitmap and you want to fill a rectangular region.</span></span>
-   <span data-ttu-id="3fb27-126">Utilisez la méthode [**ID2D1RenderTarget :: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="3fb27-126">Use the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="3fb27-127">La méthode **FillGeometry** peint l’intérieur de Geometry avec le [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)spécifié, puis applique un masque d’opacité défini par un pinceau.</span><span class="sxs-lookup"><span data-stu-id="3fb27-127">The **FillGeometry** method paints the interior of geometry with the specified [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), then applies an opacity mask, defined by a brush.</span></span> <span data-ttu-id="3fb27-128">Utilisez cette méthode lorsque vous souhaitez appliquer un masque d’opacité à une géométrie ou si vous souhaitez utiliser un pinceau comme masque d’opacité.</span><span class="sxs-lookup"><span data-stu-id="3fb27-128">Use this method when you want to apply an opacity mask to a geometry or you want to use a brush as an opacity mask.</span></span>
-   <span data-ttu-id="3fb27-129">Utilisez un [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) pour appliquer un masque d’opacité.</span><span class="sxs-lookup"><span data-stu-id="3fb27-129">Use an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) to apply an opacity mask.</span></span> <span data-ttu-id="3fb27-130">Utilisez cette approche lorsque vous souhaitez appliquer un masque d’opacité à un groupe de contenu de dessin, et pas simplement à une seule forme ou image.</span><span class="sxs-lookup"><span data-stu-id="3fb27-130">Use this approach when you want to apply an opacity mask to a group of drawing content, not just a single shape or image.</span></span> <span data-ttu-id="3fb27-131">Pour plus d’informations, consultez [vue d’ensemble des couches](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3fb27-131">For details, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a><span data-ttu-id="3fb27-132">Utiliser une image bitmap comme masque d’opacité avec la méthode FillOpacityMask</span><span class="sxs-lookup"><span data-stu-id="3fb27-132">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>

<span data-ttu-id="3fb27-133">La méthode [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) peint une zone rectangulaire d’une cible de rendu, puis applique un masque d’opacité, défini par un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="3fb27-133">The [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method paints a rectangular region of a render target and then applies an opacity mask, defined by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="3fb27-134">Utilisez cette méthode lorsque vous avez une bitmap que vous souhaitez utiliser comme masque d’opacité pour une zone rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="3fb27-134">Use this method when you have a bitmap that you want to use as an opacity mask for a rectangular region.</span></span>

<span data-ttu-id="3fb27-135">Le diagramme suivant illustre l’application du masque d’opacité (un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) avec une image de fleur) à un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) avec l’image d’une usine de Palms.</span><span class="sxs-lookup"><span data-stu-id="3fb27-135">The following diagram shows an effect of applying the opacity mask (an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with an image of a flower) to an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with an image of a fern plant.</span></span> <span data-ttu-id="3fb27-136">L’image résultante est une image bitmap d’une plante découpée en forme de fleur.</span><span class="sxs-lookup"><span data-stu-id="3fb27-136">The resulting image is a bitmap of a plant clipped to the flower shape.</span></span>

![diagramme d’une bitmap de fleur utilisée comme masque d’opacité sur une image d’une plante de Palm](images/brushes-ovw-bitmapopacity.png)

<span data-ttu-id="3fb27-138">Les exemples de code suivants montrent comment procéder.</span><span class="sxs-lookup"><span data-stu-id="3fb27-138">The following code examples shows how this is accomplished.</span></span>

<span data-ttu-id="3fb27-139">Le premier exemple charge la bitmap suivante, *m \_ pBitmapMask*, pour une utilisation en tant que masque bitmap.</span><span class="sxs-lookup"><span data-stu-id="3fb27-139">The first example loads the following bitmap, *m\_pBitmapMask*, for use as a bitmap mask.</span></span> <span data-ttu-id="3fb27-140">L’illustration suivante montre la sortie produite.</span><span class="sxs-lookup"><span data-stu-id="3fb27-140">The following illustration shows the output that is produced.</span></span> <span data-ttu-id="3fb27-141">Notez que, bien que la partie opaque de la bitmap apparaisse en noir, les informations de couleur de la bitmap n’ont aucun effet sur le masque d’opacité. seules les informations d’opacité de chaque pixel de la bitmap sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="3fb27-141">Note that, although the opaque portion of the bitmap appears black, the color information in the bitmap has no effect on the opacity mask; only the opacity information of each pixel in the bitmap is used.</span></span> <span data-ttu-id="3fb27-142">Les pixels entièrement opaques de cette bitmap ont été colorés en noir à titre d’illustration uniquement.</span><span class="sxs-lookup"><span data-stu-id="3fb27-142">The fully opaque pixels in this bitmap have been colored black for illustrative purposes only.</span></span>

![illustration du masque de bitmap de fleur](images/bitmapmask.png)

<span data-ttu-id="3fb27-144">Dans cet exemple, le [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) est chargé par une méthode d’assistance, LoadResourceBitmap, définie ailleurs dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="3fb27-144">In this example, the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is loaded by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


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



<span data-ttu-id="3fb27-145">L’exemple suivant définit le pinceau, *m \_ pFernBitmapBrush*, auquel le masque d’opacité est appliqué.</span><span class="sxs-lookup"><span data-stu-id="3fb27-145">The next example defines the brush, *m\_pFernBitmapBrush*, to which the opacity mask is applied.</span></span> <span data-ttu-id="3fb27-146">Cet exemple utilise un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) qui contient une image de Palm, mais vous pouvez utiliser à la place un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)ou [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="3fb27-146">This example uses an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that contains an image of a fern, but you could use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) instead.</span></span> <span data-ttu-id="3fb27-147">L’illustration suivante montre la sortie produite.</span><span class="sxs-lookup"><span data-stu-id="3fb27-147">The following illustration shows the output that is produced.</span></span>

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





<span data-ttu-id="3fb27-149">Maintenant que le masque d’opacité et le pinceau sont définis, vous pouvez utiliser la méthode [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) dans la méthode de rendu de votre application.</span><span class="sxs-lookup"><span data-stu-id="3fb27-149">Now that opacity mask and the brush are defined, you can use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method in your application's rendering method.</span></span> <span data-ttu-id="3fb27-150">Quand vous appelez la méthode **FillOpacityMask** , vous devez spécifier le type de masque d’opacité que vous utilisez : les **graphiques de contenu de masque d’opacité d2d1, les \_ \_ \_ \_ graphiques** de contenu de masque d’opacité **d2d1 de \_ \_ \_ \_ texte \_ naturel** et le **texte du contenu de masque d' \_ opacité d2d1 \_ \_ \_ \_ \_ compatible GDI**.</span><span class="sxs-lookup"><span data-stu-id="3fb27-150">When you call the **FillOpacityMask** method, you must specify the type of opacity mask you are using: **D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**, **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_NATURAL**, and **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_GDI\_COMPATIBLE**.</span></span> <span data-ttu-id="3fb27-151">Pour connaître la signification de ces trois types, consultez [**\_ contenu du \_ masque \_ d’opacité d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span><span class="sxs-lookup"><span data-stu-id="3fb27-151">For the meanings of these three types, see [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span></span>

> [!Note]  
> <span data-ttu-id="3fb27-152">À compter de Windows 8, [**le \_ \_ \_ contenu du masque d’opacité d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3fb27-152">Starting with Windows 8, the [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) is not required.</span></span> <span data-ttu-id="3fb27-153">Consultez la méthode [**ID2D1DeviceContext :: FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) , qui n’a aucun paramètre de **contenu de \_ \_ masque \_ d’opacité d2d1** .</span><span class="sxs-lookup"><span data-stu-id="3fb27-153">See the [**ID2D1DeviceContext::FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) method, which has no **D2D1\_OPACITY\_MASK\_CONTENT** parameter.</span></span>

 

<span data-ttu-id="3fb27-154">L’exemple suivant définit le mode d’anticrénelage de la cible de rendu sur [**d2d1 \_ mode \_ anticrénelage \_ Aliased**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) afin que le masque d’opacité fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="3fb27-154">The next example sets the render target's antialiasing mode to [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) so that the opacity mask will work properly.</span></span> <span data-ttu-id="3fb27-155">Elle appelle ensuite la méthode [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) et la transmet au masque d’opacité (*m \_ pBitmapMask*), au pinceau auquel le masque d’opacité est appliqué (*m \_ pFernBitmapBrush*), au type de contenu à l’intérieur du masque d’opacité ([**\_ \_ \_ \_ graphiques de contenu du masque d’opacité d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) et à la zone à peindre.</span><span class="sxs-lookup"><span data-stu-id="3fb27-155">It then calls the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method and passes it the opacity mask (*m\_pBitmapMask*), the brush to which the opacity mask is applied (*m\_pFernBitmapBrush*), the type of content inside the opacity mask ([**D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)), and the area to paint.</span></span> <span data-ttu-id="3fb27-156">L’illustration suivante montre la sortie produite.</span><span class="sxs-lookup"><span data-stu-id="3fb27-156">The following illustration shows the output that is produced.</span></span>

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





<span data-ttu-id="3fb27-158">Le code a été omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="3fb27-158">Code has been omitted from this example.</span></span>

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a><span data-ttu-id="3fb27-159">Utiliser un pinceau comme masque d’opacité avec la méthode FillGeometry</span><span class="sxs-lookup"><span data-stu-id="3fb27-159">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>

<span data-ttu-id="3fb27-160">La section précédente a décrit comment utiliser un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) comme masque d’opacité.</span><span class="sxs-lookup"><span data-stu-id="3fb27-160">The preceding section described how to use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) as an opacity mask.</span></span> <span data-ttu-id="3fb27-161">Direct2D fournit également la méthode [**ID2D1RenderTarget :: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , qui vous permet de spécifier éventuellement Brush comme masque d’opacité quand vous remplissez un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry).</span><span class="sxs-lookup"><span data-stu-id="3fb27-161">Direct2D also provides the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, which enables you to optionally specify brush as an opacity mask when you fill an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry).</span></span> <span data-ttu-id="3fb27-162">Cela vous permet de créer des masques d’opacité à partir de dégradés (à l’aide de [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) ou [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) et de bitmaps (à l’aide de **ID2D1Bitmap**).</span><span class="sxs-lookup"><span data-stu-id="3fb27-162">This enables you to create opacity masks from gradients (using [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) and bitmaps (using **ID2D1Bitmap**).</span></span>

<span data-ttu-id="3fb27-163">La méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) accepte trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="3fb27-163">The [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method takes three parameters:</span></span>

-   <span data-ttu-id="3fb27-164">Le premier paramètre, [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), définit la forme à peindre.</span><span class="sxs-lookup"><span data-stu-id="3fb27-164">The first parameter, an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), defines the shape to paint.</span></span>
-   <span data-ttu-id="3fb27-165">Le deuxième paramètre, [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), spécifie le pinceau utilisé pour peindre la géométrie.</span><span class="sxs-lookup"><span data-stu-id="3fb27-165">The second parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies the brush used to paint the geometry.</span></span> <span data-ttu-id="3fb27-166">Ce paramètre doit être un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) dont les modes x et y sont définis sur le mode d' [**extension \_ d2d1 \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="3fb27-166">This parameter must be an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that has its x- and y-extend modes set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>
-   <span data-ttu-id="3fb27-167">Le troisième paramètre, [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), spécifie un pinceau à utiliser comme masque d’opacité.</span><span class="sxs-lookup"><span data-stu-id="3fb27-167">The third parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies a brush to use as the opacity mask.</span></span> <span data-ttu-id="3fb27-168">Ce pinceau peut être [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)ou [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="3fb27-168">This brush may be an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), or an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span> <span data-ttu-id="3fb27-169">(Techniquement, vous pouvez utiliser un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), mais l’utilisation d’un pinceau de couleur unie comme masque d’opacité ne produit pas de résultats intéressants.)</span><span class="sxs-lookup"><span data-stu-id="3fb27-169">(Technically, you may use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), but using a solid color brush as an opacity mask doesn't produce interesting results.)</span></span>

<span data-ttu-id="3fb27-170">Les sections suivantes décrivent comment utiliser les objets [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) et [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) en tant que masques d’opacité.</span><span class="sxs-lookup"><span data-stu-id="3fb27-170">The following sections describe how to use [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) and [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) objects as opacity masks.</span></span>

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="3fb27-171">Utiliser un pinceau de dégradé linéaire comme masque d’opacité</span><span class="sxs-lookup"><span data-stu-id="3fb27-171">Use an Linear Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="3fb27-172">Le diagramme suivant illustre l’effet de l’application d’un pinceau de dégradé linéaire à un rectangle rempli d’une image bitmap de fleurs.</span><span class="sxs-lookup"><span data-stu-id="3fb27-172">The following diagram shows the effect of applying a linear gradient brush to a rectangle that is filled with a bitmap of flowers.</span></span>

![diagramme d’une image bitmap de fleur avec un pinceau dégradé linéaire appliqué](images/brushes-ovw-lineargradient-opacitymask.png)

<span data-ttu-id="3fb27-174">Les étapes qui suivent décrivent comment recréer cet effet.</span><span class="sxs-lookup"><span data-stu-id="3fb27-174">The steps that follow describe how to re-create this effect.</span></span>

1.  <span data-ttu-id="3fb27-175">Définissez le contenu à masquer.</span><span class="sxs-lookup"><span data-stu-id="3fb27-175">Define the content to be masked.</span></span> <span data-ttu-id="3fb27-176">L’exemple suivant crée un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pLinearFadeFlowersBitmap*.</span><span class="sxs-lookup"><span data-stu-id="3fb27-176">The following example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pLinearFadeFlowersBitmap*.</span></span> <span data-ttu-id="3fb27-177">Le mode étendu x et y-pour *m \_ pLinearFadeFlowersBitmap* sont définis sur le [**\_ mode d' \_ extension \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) pour qu’il puisse être utilisé avec un masque d’opacité par la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="3fb27-177">The extend mode x- and y- for *m\_pLinearFadeFlowersBitmap* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) so that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

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
    <th><span data-ttu-id="3fb27-178">C++</span><span class="sxs-lookup"><span data-stu-id="3fb27-178">C++</span></span></th>
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
    <th><span data-ttu-id="3fb27-179">C++</span><span class="sxs-lookup"><span data-stu-id="3fb27-179">C++</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  <span data-ttu-id="3fb27-180">Définissez le masque d’opacité.</span><span class="sxs-lookup"><span data-stu-id="3fb27-180">Define the opacity mask.</span></span> <span data-ttu-id="3fb27-181">L’exemple de code suivant crée un pinceau dégradé linéaire Diagonal (*m \_ pLinearGradientBrush*) qui apparaît en fondu du noir entièrement opaque à la position 0 au blanc complètement transparent à la position 1.</span><span class="sxs-lookup"><span data-stu-id="3fb27-181">The next code example creates a diagonal linear gradient brush (*m\_pLinearGradientBrush*) that fades from fully opaque black at position 0 to completely transparent white at position 1.</span></span>
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



    

3.  <span data-ttu-id="3fb27-182">Utilisez la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="3fb27-182">Use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="3fb27-183">L’exemple final utilise la méthode **FillGeometry** dans le pinceau de contenu pour remplir [**un ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) avec un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pLinearFadeFlowersBitmap*) et applique un masque d’opacité (*m \_ pLinearGradientBrush*).</span><span class="sxs-lookup"><span data-stu-id="3fb27-183">The final example uses the **FillGeometry** method to the content brush to fill a [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*) with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pLinearFadeFlowersBitmap*) and applies an opacity mask (*m\_pLinearGradientBrush*).</span></span>
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

<span data-ttu-id="3fb27-184">Le code a été omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="3fb27-184">Code has been omitted from this example.</span></span>

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="3fb27-185">Utiliser un pinceau de dégradé radial comme masque d’opacité</span><span class="sxs-lookup"><span data-stu-id="3fb27-185">Use a Radial Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="3fb27-186">Le diagramme suivant illustre l’effet visuel de l’application d’un pinceau de dégradé radial à un rectangle rempli avec une bitmap de feuillage.</span><span class="sxs-lookup"><span data-stu-id="3fb27-186">The following diagram shows the visual effect of applying a radial gradient brush to a rectangle that is filled with a bitmap of foliage.</span></span>

![diagramme d’une bitmap de feuillage avec un pinceau de dégradé radial appliqué](images/brushes-ovw-radialgradient-opacitymask.png)

<span data-ttu-id="3fb27-188">Le premier exemple crée un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pRadialFadeFlowersBitmapBrush*.</span><span class="sxs-lookup"><span data-stu-id="3fb27-188">The first example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pRadialFadeFlowersBitmapBrush*.</span></span> <span data-ttu-id="3fb27-189">Pour qu’il puisse être utilisé avec un masque d’opacité par la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , le mode d’extension x et y-pour *m \_ pRadialFadeFlowersBitmapBrush* sont définis sur le mode d' [**extension d2d1 \_ \_ \_ clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="3fb27-189">So that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, the extend mode x- and y- for *m\_pRadialFadeFlowersBitmapBrush* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>


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
<th><span data-ttu-id="3fb27-190">C++</span><span class="sxs-lookup"><span data-stu-id="3fb27-190">C++</span></span></th>
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
<th><span data-ttu-id="3fb27-191">C++</span><span class="sxs-lookup"><span data-stu-id="3fb27-191">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="3fb27-192">L’exemple suivant définit le pinceau de dégradé radial qui sera utilisé comme masque d’opacité.</span><span class="sxs-lookup"><span data-stu-id="3fb27-192">The next example defines the radial gradient brush that will be used as the opacity mask.</span></span>


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





<span data-ttu-id="3fb27-193">L’exemple de code final utilise [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pRadialFadeFlowersBitmapBrush*) et le masque d’opacité (*m \_ pRadialGradientBrush*) pour remplir un [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*).</span><span class="sxs-lookup"><span data-stu-id="3fb27-193">The final code example uses the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pRadialFadeFlowersBitmapBrush*) and the opacity mask (*m\_pRadialGradientBrush*) to fill an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*).</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



<span data-ttu-id="3fb27-194">Le code a été omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="3fb27-194">Code has been omitted from this example.</span></span>

## <a name="apply-an-opacity-mask-to-a-layer"></a><span data-ttu-id="3fb27-195">Appliquer un masque d’opacité à une couche</span><span class="sxs-lookup"><span data-stu-id="3fb27-195">Apply an Opacity Mask to a Layer</span></span>

<span data-ttu-id="3fb27-196">Quand vous appelez [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) pour pousser un [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) sur une cible de rendu, vous pouvez utiliser la structure des [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) pour appliquer un pinceau comme masque d’opacité.</span><span class="sxs-lookup"><span data-stu-id="3fb27-196">When you call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) to push an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) onto an render target, you can use the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to apply a brush as an opacity mask.</span></span> <span data-ttu-id="3fb27-197">L’exemple de code suivant utilise un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) comme masque d’opacité.</span><span class="sxs-lookup"><span data-stu-id="3fb27-197">The following code example uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) as an opacity mask.</span></span>


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



<span data-ttu-id="3fb27-198">Pour plus d’informations sur l’utilisation des couches, consultez [vue d’ensemble des couches](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3fb27-198">For more information about using layers, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fb27-199">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3fb27-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fb27-200">Vue d’ensemble des pinceaux</span><span class="sxs-lookup"><span data-stu-id="3fb27-200">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="3fb27-201">Vue d’ensemble des couches</span><span class="sxs-lookup"><span data-stu-id="3fb27-201">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

 

 