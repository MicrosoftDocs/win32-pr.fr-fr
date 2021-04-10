---
title: Vue d’ensemble des cibles de rendu a8 compatibles
description: Décrit les principes de base des cibles de rendu a8 compatibles et fournit des exemples montrant comment les utiliser.
ms.assetid: 218c0123-8da9-4d73-9882-cbf7f205001f
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 552577283adfa9a440e94b7e04f4056bd6c3ecda
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "103941531"
---
# <a name="compatible-a8-render-targets-overview"></a><span data-ttu-id="4eb55-103">Vue d’ensemble des cibles de rendu a8 compatibles</span><span class="sxs-lookup"><span data-stu-id="4eb55-103">Compatible A8 render targets overview</span></span>

<span data-ttu-id="4eb55-104">Cette rubrique décrit les principes de base d’une cible de rendu a8 compatible et fournit des exemples d’utilisation de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="4eb55-104">This topic describes the basics of a compatible A8 render target, and provides examples of how to use it.</span></span>

<span data-ttu-id="4eb55-105">Une cible de rendu a8 compatible est une cible de rendu compatible ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)) qui utilise un format de pixel A8 ( \_ format dxgi \_ a8 \_ UNORM).</span><span class="sxs-lookup"><span data-stu-id="4eb55-105">A compatible A8 render target is a compatible render target ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)) that uses an A8 pixel format (DXGI\_FORMAT\_A8\_UNORM).</span></span> <span data-ttu-id="4eb55-106">Vous pouvez utiliser une cible de rendu a8 compatible pour améliorer les performances de l’application et fournir des transitions plus lisses pendant l’animation de texte.</span><span class="sxs-lookup"><span data-stu-id="4eb55-106">You can use a compatible A8 render target to improve the application's performance and provide smoother transitions during text animation.</span></span> <span data-ttu-id="4eb55-107">Une cible de rendu a8 compatible est particulièrement utile lorsque vous essayez d’améliorer les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="4eb55-107">A compatible A8 render target is particular useful when you try to improve the following:</span></span>

-   <span data-ttu-id="4eb55-108">Fréquence d’images de l’application qui restitue le texte ou la géométrie avec anticrénelage qui comprend uniquement des animations simples, telles que des modifications de translation, de rotation, de mise à l’échelle ou de couleur.</span><span class="sxs-lookup"><span data-stu-id="4eb55-108">The frame rate of the application that renders text or anti-aliased geometry that includes only simple animations, such as translation, rotation, scale, or color changes.</span></span>

-   <span data-ttu-id="4eb55-109">Continuité visuelle de l’application qui étire et diminshes le texte pendant une animation.</span><span class="sxs-lookup"><span data-stu-id="4eb55-109">The visual continuity of the application that stretches and diminshes text during an animation.</span></span>

<span data-ttu-id="4eb55-110">Pour créer une cible de rendu a8 compatible, utilisez la méthode [**ID2D1RenderTarget :: CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) avec le format \_ dxgi \_ a8 \_ UNORM pixel format et spécifiez une cible de rendu compatible retournée.</span><span class="sxs-lookup"><span data-stu-id="4eb55-110">To create a compatible A8 render target, use the [**ID2D1RenderTarget::CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) method together with the DXGI\_FORMAT\_A8\_UNORM pixel format, and specify a returned compatible render target.</span></span> <span data-ttu-id="4eb55-111">Pour plus d’informations sur les formats de pixel, consultez [formats de pixel pris en charge et modes alpha](./supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="4eb55-111">For more information about pixel formats, see [Supported pixel formats and alpha modes](./supported-pixel-formats-and-alpha-modes.md).</span></span>

<span data-ttu-id="4eb55-112">Par exemple, pour animer efficacement le texte affiché dans la capture d’écran suivante, utilisez une cible de rendu a8 compatible pour mettre en cache le texte en tant que masque d’opacité.</span><span class="sxs-lookup"><span data-stu-id="4eb55-112">For example, to efficiently animate the text that is shown in the following screen shot, use a compatible A8 render target to cache the text as an opacity mask.</span></span> <span data-ttu-id="4eb55-113">Ensuite, appliquez des transformations au masque d’opacité pour obtenir des résultats de rendu rapides.</span><span class="sxs-lookup"><span data-stu-id="4eb55-113">Then, apply transformations to the opacity mask to achieve fast rendering results.</span></span>

![capture d’écran du texte à animer](images/a8rendertarget.png)

<span data-ttu-id="4eb55-115">Le code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="4eb55-115">The following code shows how to do this.</span></span> <span data-ttu-id="4eb55-116">Elle crée une cible de rendu a8 compatible, récupère la bitmap à partir de celle-ci, puis restitue la bitmap à l’aide de [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md).</span><span class="sxs-lookup"><span data-stu-id="4eb55-116">It creates a compatible A8 render target, retrieves the bitmap from it, and then renders the bitmap by using [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md).</span></span>

```cpp
ID2D1BitmapRenderTarget *m_pOpacityRT;

// Create the compatible render target using desiredPixelSize to avoid
// blurriness issues caused by a fractional-pixel desiredSize.

D2D1_PIXEL_FORMAT alphaOnlyFormat = D2D1::PixelFormat(
    DXGI_FORMAT_A8_UNORM, 
    D2D1_ALPHA_MODE_PREMULTIPLIED);

hr = m_pRT->CreateCompatibleRenderTarget(
    NULL,
    &maskPixelSize,
    &alphaOnlyFormat,
    D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE,
    &m_pOpacityRT
    );

D2D1_RECT_F destinationRect = D2D1::RectF(
    roundedOffset.x,
    roundedOffset.y,
    roundedOffset.x + opacityRTSize.width,
    roundedOffset.y + opacityRTSize.height
    );

ID2D1Bitmap *pBitmap = NULL;
m_pOpacityRT->GetBitmap(&pBitmap);

pBitmap->GetDpi(&dpiX, &dpiY);

// The antialias mode must be set to D2D1_ANTIALIAS_MODE_ALIASED
// for this method to succeed. We've set this mode already though
// so no need to do it again.

m_pRT->FillOpacityMask(
    pBitmap,
    m_pBlackBrush,
    D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL,
    &destinationRect
    );

pBitmap->Release();
```

## <a name="related-topics"></a><span data-ttu-id="4eb55-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4eb55-117">Related topics</span></span>

[<span data-ttu-id="4eb55-118">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="4eb55-118">Direct2D Reference</span></span>](reference.md)