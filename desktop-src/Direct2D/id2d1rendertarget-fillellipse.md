---
title: Méthodes ID2D1RenderTarget FillEllipse (D2d1. h)
description: Peint l’intérieur de l’ellipse spécifiée.
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
keywords:
- Méthodes FillEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b8328775d87dd4df0fd015990d31db0751b729bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545363"
---
# <a name="id2d1rendertargetfillellipse-methods"></a><span data-ttu-id="ea26d-104">ID2D1RenderTarget :: FillEllipse, méthodes</span><span class="sxs-lookup"><span data-stu-id="ea26d-104">ID2D1RenderTarget::FillEllipse methods</span></span>

<span data-ttu-id="ea26d-105">Peint l’intérieur de l’ellipse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ea26d-105">Paints the interior of the specified ellipse.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ea26d-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="ea26d-106">Overload list</span></span>



| <span data-ttu-id="ea26d-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="ea26d-107">Method</span></span>                                                                                                             | <span data-ttu-id="ea26d-108">Description</span><span class="sxs-lookup"><span data-stu-id="ea26d-108">Description</span></span>                                               |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span data-ttu-id="ea26d-109">[**FillEllipse (D2D1 \_ ELLIPSE&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="ea26d-109">[**FillEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span>  | <span data-ttu-id="ea26d-110">Peint l’intérieur de l’ellipse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ea26d-110">Paints the interior of the specified ellipse.</span></span> <br/> |
| <span data-ttu-id="ea26d-111">[**FillEllipse (D2D1 \_ ellipse \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="ea26d-111">[**FillEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span> | <span data-ttu-id="ea26d-112">Peint l’intérieur de l’ellipse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ea26d-112">Paints the interior of the specified ellipse.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="ea26d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ea26d-113">Remarks</span></span>

<span data-ttu-id="ea26d-114">Cette méthode ne retourne pas de code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="ea26d-114">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="ea26d-115">Pour déterminer si une opération de dessin (telle que **FillEllipse**) a échoué, vérifiez les résultats retournés par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="ea26d-115">To determine whether a drawing operation (such as **FillEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="ea26d-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="ea26d-116">Examples</span></span>

<span data-ttu-id="ea26d-117">Pour obtenir un exemple, consultez [Comment dessiner et remplir une forme de base](how-to-draw-an-ellipse.md).</span><span class="sxs-lookup"><span data-stu-id="ea26d-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea26d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea26d-118">Requirements</span></span>



| <span data-ttu-id="ea26d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea26d-119">Requirement</span></span> | <span data-ttu-id="ea26d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea26d-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ea26d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea26d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ea26d-122"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea26d-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea26d-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea26d-123">Library</span></span><br/> | <dl> <span data-ttu-id="ea26d-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea26d-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="ea26d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ea26d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="ea26d-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea26d-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea26d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea26d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea26d-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="ea26d-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="ea26d-129">Comment dessiner et remplir une forme de base</span><span class="sxs-lookup"><span data-stu-id="ea26d-129">How to Draw and Fill a Basic Shape</span></span>](how-to-draw-an-ellipse.md)
</dt> </dl>

<span data-ttu-id="ea26d-130">�</span><span class="sxs-lookup"><span data-stu-id="ea26d-130">�</span></span>

<span data-ttu-id="ea26d-131">�</span><span class="sxs-lookup"><span data-stu-id="ea26d-131">�</span></span>
