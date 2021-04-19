---
title: Méthodes ID2D1RenderTarget PushAxisAlignedClip (D2d1 \_ 1. h)
description: Spécifie un rectangle dans lequel toutes les opérations de dessin suivantes sont découpées.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Méthodes PushAxisAlignedClip Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: d7e6d59f1c4cbffcde74ecb7b5adb5b12eff06bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541536"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a><span data-ttu-id="e31b8-104">ID2D1RenderTarget ::P méthodes ushAxisAlignedClip</span><span class="sxs-lookup"><span data-stu-id="e31b8-104">ID2D1RenderTarget::PushAxisAlignedClip methods</span></span>

<span data-ttu-id="e31b8-105">Spécifie un rectangle dans lequel toutes les opérations de dessin suivantes sont découpées.</span><span class="sxs-lookup"><span data-stu-id="e31b8-105">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span>

### <a name="overload-list"></a><span data-ttu-id="e31b8-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="e31b8-106">Overload list</span></span>



| <span data-ttu-id="e31b8-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="e31b8-107">Method</span></span>                                                                                                                                         | <span data-ttu-id="e31b8-108">Description</span><span class="sxs-lookup"><span data-stu-id="e31b8-108">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31b8-109">[**PushAxisAlignedClip (D2D1 \_ rect \_ F&, \_ mode antialias d2d1 \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="e31b8-109">[**PushAxisAlignedClip(D2D1\_RECT\_F&,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span>  | <span data-ttu-id="e31b8-110">Spécifie un rectangle dans lequel toutes les opérations de dessin suivantes sont découpées.</span><span class="sxs-lookup"><span data-stu-id="e31b8-110">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |
| <span data-ttu-id="e31b8-111">[**PushAxisAlignedClip (D2D1 \_ rect \_ F \* , \_ mode anticrénelage d2d1 \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="e31b8-111">[**PushAxisAlignedClip(D2D1\_RECT\_F\*,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span> | <span data-ttu-id="e31b8-112">Spécifie un rectangle dans lequel toutes les opérations de dessin suivantes sont découpées.</span><span class="sxs-lookup"><span data-stu-id="e31b8-112">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="e31b8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e31b8-113">Remarks</span></span>

<span data-ttu-id="e31b8-114">Une paire [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) et [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) peut se produire autour ou dans un [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) et [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), mais ne peut pas se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="e31b8-114">A [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pair can occur around or within a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), but cannot overlap.</span></span> <span data-ttu-id="e31b8-115">Par exemple, la séquence de **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** est valide, mais la séquence de **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e31b8-115">For example, the sequence of **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** is valid, but the sequence of **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** is invalid.</span></span>

<span data-ttu-id="e31b8-116">Cette méthode ne retourne pas de code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="e31b8-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="e31b8-117">Pour déterminer si une opération de dessin (telle que **PushAxisAlignedClip**) a échoué, vérifiez le résultat retourné par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="e31b8-117">To determine whether a drawing operation (such as **PushAxisAlignedClip**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="e31b8-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="e31b8-118">Examples</span></span>

<span data-ttu-id="e31b8-119">Pour obtenir un exemple, consultez la section [How to clip with a Axis-Aligned Clip Rectangle](how-to-clip-with-axis-aligned-rects.md).</span><span class="sxs-lookup"><span data-stu-id="e31b8-119">For an example, see the [How to Clip with an Axis-Aligned Clip Rectangle](how-to-clip-with-axis-aligned-rects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e31b8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e31b8-120">Requirements</span></span>



| <span data-ttu-id="e31b8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e31b8-121">Requirement</span></span> | <span data-ttu-id="e31b8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e31b8-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31b8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e31b8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e31b8-124"><dt>D2d1 \_ 1. h (inclure D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e31b8-124"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="e31b8-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e31b8-125">Library</span></span><br/> | <dl> <span data-ttu-id="e31b8-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e31b8-126"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e31b8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e31b8-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="e31b8-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e31b8-128"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="e31b8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e31b8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31b8-130">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e31b8-130">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

<span data-ttu-id="e31b8-131">�</span><span class="sxs-lookup"><span data-stu-id="e31b8-131">�</span></span>

<span data-ttu-id="e31b8-132">�</span><span class="sxs-lookup"><span data-stu-id="e31b8-132">�</span></span>
