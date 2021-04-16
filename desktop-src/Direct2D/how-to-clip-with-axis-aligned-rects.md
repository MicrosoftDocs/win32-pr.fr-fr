---
title: Comment découper avec un rectangle de découpage Axis-Aligned
description: Montre comment découper une zone avec un rectangle de découpage aligné sur l’axe.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9fea904f9df396918d2cdfdb5205f6dd0197d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104566276"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a><span data-ttu-id="e318e-103">Comment découper avec un rectangle de découpage Axis-Aligned</span><span class="sxs-lookup"><span data-stu-id="e318e-103">How to Clip with an Axis-Aligned Clip Rectangle</span></span>

<span data-ttu-id="e318e-104">Cette rubrique explique comment découper une image avec un rectangle de découpage aligné sur l’axe.</span><span class="sxs-lookup"><span data-stu-id="e318e-104">This topic describes how to clip an image with an axis-aligned clip rectangle.</span></span> <span data-ttu-id="e318e-105">Cette approche produit uniquement des clips rectangulaires, car les limites de contenu sont alignées sur l’axe du rectangle.</span><span class="sxs-lookup"><span data-stu-id="e318e-105">This approach produces only rectangular clips, because the content bounds are aligned to the axis of the rectangle.</span></span> <span data-ttu-id="e318e-106">Cette approche est plus efficace que l’utilisation de couches avec les limites du contenu.</span><span class="sxs-lookup"><span data-stu-id="e318e-106">This approach is more efficient than using layers with the content bounds.</span></span> <span data-ttu-id="e318e-107">Pour plus d’informations, consultez[vue d’ensemble des couches](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e318e-107">For more information, see[Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="e318e-108">**Pour découper avec un rectangle de découpage aligné sur l’axe**</span><span class="sxs-lookup"><span data-stu-id="e318e-108">**To clip with an axis-aligned clip rectangle**</span></span>

1.  <span data-ttu-id="e318e-109">Chargez l’image d’origine à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="e318e-109">Load the original image from a resource.</span></span> <span data-ttu-id="e318e-110">Pour plus d’informations sur le chargement d’une image bitmap, consultez [Comment charger une image bitmap à partir d’une ressource](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="e318e-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="e318e-111">Appelez [**ID2D1RenderTarget ::P ushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) pour spécifier un rectangle.</span><span class="sxs-lookup"><span data-stu-id="e318e-111">Call [**ID2D1RenderTarget::PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) to specify a rectangle.</span></span> <span data-ttu-id="e318e-112">Les commandes de rendu sont découpées dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="e318e-112">The rendering commands are clipped to the rectangle.</span></span>

3.  <span data-ttu-id="e318e-113">Peignez l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="e318e-113">Paint the original image.</span></span>
4.  <span data-ttu-id="e318e-114">Appelez [**ID2D1RenderTarget ::P opaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pour supprimer le dernier élément aligné sur l’axe de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="e318e-114">Call [**ID2D1RenderTarget::PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the last axis-aligned clip from the render target.</span></span>

<span data-ttu-id="e318e-115">Par exemple, dans l’illustration suivante, le bitmap d’origine sur la gauche est 200 \* 130 pixels.</span><span class="sxs-lookup"><span data-stu-id="e318e-115">For example, in the following illustration, the original bitmap on the left is 200\*130 pixels.</span></span> <span data-ttu-id="e318e-116">L’image bitmap de droite est la bitmap d’origine découpée vers le rectangle de découpage aligné sur l’axe.</span><span class="sxs-lookup"><span data-stu-id="e318e-116">The bitmap on the right is the original bitmap clipped to the axis-aligned clip rectangle.</span></span> <span data-ttu-id="e318e-117">Les dimensions sont (20, 20) à (100, 100).</span><span class="sxs-lookup"><span data-stu-id="e318e-117">The dimensions are (20, 20) to (100, 100).</span></span>

![illustration d’une image bitmap Goldfish avant et après le découpage de la bitmap](images/cliparegion-axisalignedclip.png)

<span data-ttu-id="e318e-119">Pour créer l’image découpée, créez une structure Rectangle comme zone de découpage.</span><span class="sxs-lookup"><span data-stu-id="e318e-119">To create the clipped image, create a rectangle structure as the clipping area.</span></span> <span data-ttu-id="e318e-120">Appelez [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) avec la zone de découpage et peignez l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="e318e-120">Call [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) with the clipping area and paint the original image.</span></span> <span data-ttu-id="e318e-121">Appelez [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pour supprimer le clip de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="e318e-121">Call [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the clip from the render target.</span></span> <span data-ttu-id="e318e-122">Le code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="e318e-122">The following code shows how to do this.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a><span data-ttu-id="e318e-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e318e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e318e-124">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="e318e-124">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 