---
title: Méthodes ID2D1RenderTarget FillOpacityMask
description: Applique le masque d’opacité décrit par l’image bitmap spécifiée à un pinceau et utilise ce pinceau pour peindre une région de la cible de rendu.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- Méthodes FillOpacityMask Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: e988994b849c193725dfdd75773f22a63fed6754
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542458"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a><span data-ttu-id="38f07-104">ID2D1RenderTarget :: FillOpacityMask, méthodes</span><span class="sxs-lookup"><span data-stu-id="38f07-104">ID2D1RenderTarget::FillOpacityMask methods</span></span>

<span data-ttu-id="38f07-105">Applique le masque d’opacité décrit par l’image bitmap spécifiée à un pinceau et utilise ce pinceau pour peindre une région de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="38f07-105">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span>

### <a name="overload-list"></a><span data-ttu-id="38f07-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="38f07-106">Overload list</span></span>



| <span data-ttu-id="38f07-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="38f07-107">Method</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="38f07-108">Description</span><span class="sxs-lookup"><span data-stu-id="38f07-108">Description</span></span>                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38f07-109">[**FillOpacityMask (ID2D1Bitmap \* , ID2D1Brush \* , d2d1 le \_ contenu du masque d’opacité \_ \_ , D2D \_ rect \_ f&, D2D \_ rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="38f07-109">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F&,D2D\_RECT\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span></span>       | <span data-ttu-id="38f07-110">Applique le masque d’opacité décrit par l’image bitmap spécifiée à un pinceau et utilise ce pinceau pour peindre une région de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="38f07-110">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |
| <span data-ttu-id="38f07-111">[**FillOpacityMask (ID2D1Bitmap \* , ID2D1Brush \* , d2d1 le \_ contenu du masque d’opacité \_ \_ , D2D \_ rect \_ f \* , D2D \_ rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="38f07-111">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F\*,D2D\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span></span> | <span data-ttu-id="38f07-112">Applique le masque d’opacité décrit par l’image bitmap spécifiée à un pinceau et utilise ce pinceau pour peindre une région de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="38f07-112">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="38f07-113">Notes</span><span class="sxs-lookup"><span data-stu-id="38f07-113">Remarks</span></span>

<span data-ttu-id="38f07-114">Pour que cette méthode fonctionne correctement, la cible de rendu doit utiliser le mode d’anticrénelage [**\_ \_ \_ alias d2d1 mode**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="38f07-114">For this method to work properly, the render target must be using the [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) antialiasing mode.</span></span> <span data-ttu-id="38f07-115">Vous pouvez définir le mode d’anticrénelage en appelant la méthode [**ID2D1RenderTarget :: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) .</span><span class="sxs-lookup"><span data-stu-id="38f07-115">You can set the antialiasing mode by calling the [**ID2D1RenderTarget::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) method.</span></span>

<span data-ttu-id="38f07-116">Cette méthode ne retourne pas de code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="38f07-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="38f07-117">Pour déterminer si une opération de dessin (telle que **FillOpacityMask**) a échoué, vérifiez le résultat retourné par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="38f07-117">To determine whether a drawing operation (such as **FillOpacityMask**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="38f07-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38f07-118">Requirements</span></span>



| <span data-ttu-id="38f07-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38f07-119">Requirement</span></span> | <span data-ttu-id="38f07-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="38f07-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="38f07-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="38f07-121">Library</span></span><br/> | <dl> <span data-ttu-id="38f07-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38f07-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="38f07-123">DLL</span><span class="sxs-lookup"><span data-stu-id="38f07-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="38f07-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38f07-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38f07-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38f07-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f07-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="38f07-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

