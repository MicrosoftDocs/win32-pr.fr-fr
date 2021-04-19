---
title: Méthodes ID2D1RenderTarget DrawEllipse (D2d1. h)
description: Dessine le contour d’une ellipse avec les dimensions et le trait spécifiés.
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- Méthodes DrawEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9647591b5033b912283500a0ddb1dba20004ec38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523527"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a><span data-ttu-id="153ba-104">ID2D1RenderTarget ::D méthodes rawEllipse</span><span class="sxs-lookup"><span data-stu-id="153ba-104">ID2D1RenderTarget::DrawEllipse methods</span></span>

<span data-ttu-id="153ba-105">Dessine le contour d’une ellipse avec les dimensions et le trait spécifiés.</span><span class="sxs-lookup"><span data-stu-id="153ba-105">Draws the outline of an ellipse with the specified dimensions and stroke.</span></span>

### <a name="overload-list"></a><span data-ttu-id="153ba-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="153ba-106">Overload list</span></span>



| <span data-ttu-id="153ba-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="153ba-107">Method</span></span>                                                                                                                                                                 | <span data-ttu-id="153ba-108">Description</span><span class="sxs-lookup"><span data-stu-id="153ba-108">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span data-ttu-id="153ba-109">[**DrawEllipse (D2D1 \_ ELLIPSE&, ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="153ba-109">[**DrawEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span>  | <span data-ttu-id="153ba-110">Dessine le contour de l’ellipse spécifiée à l’aide du style de trait spécifié.</span><span class="sxs-lookup"><span data-stu-id="153ba-110">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |
| <span data-ttu-id="153ba-111">[**DrawEllipse (D2D1 \_ ellipse \* , ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="153ba-111">[**DrawEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span> | <span data-ttu-id="153ba-112">Dessine le contour de l’ellipse spécifiée à l’aide du style de trait spécifié.</span><span class="sxs-lookup"><span data-stu-id="153ba-112">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="153ba-113">Notes</span><span class="sxs-lookup"><span data-stu-id="153ba-113">Remarks</span></span>

<span data-ttu-id="153ba-114">La méthode **DrawEllipse** ne retourne pas de code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="153ba-114">The **DrawEllipse** method doesn't return an error code if it fails.</span></span> <span data-ttu-id="153ba-115">Pour déterminer si une opération de dessin (telle que **DrawEllipse**) a échoué, vérifiez le résultat retourné par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="153ba-115">To determine whether a drawing operation (such as **DrawEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="153ba-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="153ba-116">Examples</span></span>

<span data-ttu-id="153ba-117">Pour obtenir un exemple, consultez [Comment dessiner et remplir une forme de base](how-to-draw-an-ellipse.md).</span><span class="sxs-lookup"><span data-stu-id="153ba-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="153ba-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="153ba-118">Requirements</span></span>



| <span data-ttu-id="153ba-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="153ba-119">Requirement</span></span> | <span data-ttu-id="153ba-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="153ba-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="153ba-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="153ba-121">Header</span></span><br/>  | <dl> <span data-ttu-id="153ba-122"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="153ba-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="153ba-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="153ba-123">Library</span></span><br/> | <dl> <span data-ttu-id="153ba-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="153ba-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="153ba-125">DLL</span><span class="sxs-lookup"><span data-stu-id="153ba-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="153ba-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="153ba-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="153ba-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="153ba-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153ba-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="153ba-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

<span data-ttu-id="153ba-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="153ba-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span></span>
</dt> </dl>

<span data-ttu-id="153ba-130">�</span><span class="sxs-lookup"><span data-stu-id="153ba-130">�</span></span>

<span data-ttu-id="153ba-131">�</span><span class="sxs-lookup"><span data-stu-id="153ba-131">�</span></span>
